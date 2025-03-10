---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Sessions
schema: 2.0.0
---

# Enable-PodeSessionMiddleware

## SYNOPSIS
Enables Middleware for creating, retrieving and using Sessions within Pode.

## SYNTAX

### Cookies (Default)
```
Enable-PodeSessionMiddleware [-Secret <String>] [-Name <String>] [-Duration <Int32>] [-Generator <ScriptBlock>]
 [-Storage <PSObject>] [-Scope <String>] [-Extend] [-HttpOnly] [-Secure] [-Strict]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Headers
```
Enable-PodeSessionMiddleware [-Secret <String>] [-Name <String>] [-Duration <Int32>] [-Generator <ScriptBlock>]
 [-Storage <PSObject>] [-Scope <String>] [-Extend] [-Strict] [-UseHeaders] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Enables Middleware for creating, retrieving and using Sessions within Pode; with support for defining Session duration, and custom Storage.
If you're storing sessions outside of Pode, you must supply a Secret value so sessions aren't corrupted.

## EXAMPLES

### EXAMPLE 1
```
Enable-PodeSessionMiddleware -Duration 120
```

### EXAMPLE 2
```
Enable-PodeSessionMiddleware -Duration 120 -Extend -Generator { return [System.IO.Path]::GetRandomFileName() }
```

### EXAMPLE 3
```
Enable-PodeSessionMiddleware -Secret 'schwifty' -Duration 120 -UseHeaders -Strict
```

## PARAMETERS

### -Duration
The duration a Session should last for, before being expired.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Extend
If supplied, the Sessions will have their durations extended on each successful Request.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Generator
A custom ScriptBlock to generate a random unique SessionId.
The value returned must be a String.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpOnly
If supplied, the Session cookie will only be accessible to browsers.

```yaml
Type: SwitchParameter
Parameter Sets: Cookies
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the cookie/header used for the Session.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Pode.sid
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressAction
{{ Fill ProgressAction Description }}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: proga

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
The Scope that the Session applies to, possible values are Browser and Tab (Default: Browser).
The Browser scope is the default logic, where authentication and general data for the sessions are shared across all tabs.
The Tab scope keep the authentication data shared across all tabs, but general data is separated across different tabs.
For the Tab scope, the "Tab ID" required will be sourced from the "X-PODE-SESSION-TAB-ID" header.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Browser
Accept pipeline input: False
Accept wildcard characters: False
```

### -Secret
An optional Secret to use when signing Sessions (Default: random GUID).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Secure
If supplied, the Session cookie will only be accessible over HTTPS Requests.

```yaml
Type: SwitchParameter
Parameter Sets: Cookies
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Storage
A custom PSObject that defines methods for Delete, Get, and Set.
This allow you to store Sessions in custom Storage such as Redis.
A Secret is required.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Strict
If supplied, the Secret will be extended using the client request's UserAgent and RemoteIPAddress.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseHeaders
If supplied, Sessions will be sent back in a header on the Response with the Name supplied.

```yaml
Type: SwitchParameter
Parameter Sets: Headers
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
