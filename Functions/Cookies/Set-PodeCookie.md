---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Cookies
schema: 2.0.0
---

# Set-PodeCookie

## SYNOPSIS
Sets a cookie on the Response.

## SYNTAX

### Duration (Default)
```
Set-PodeCookie -Name <String> [-Value <String>] [-Secret <String>] [-Duration <Int32>] [-HttpOnly] [-Discard]
 [-Secure] [-Strict] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ExpiryDate
```
Set-PodeCookie -Name <String> [-Value <String>] [-Secret <String>] [-ExpiryDate <DateTime>] [-HttpOnly]
 [-Discard] [-Secure] [-Strict] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Sets a cookie on the Response using the "Set-Cookie" header.
You can also set cookies to expire, or being signed.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeCookie -Name 'Views' -Value 2
```

### EXAMPLE 2
```
Set-PodeCookie -Name 'Views' -Value 2 -Secret 'hunter2'
```

### EXAMPLE 3
```
Set-PodeCookie -Name 'Views' -Value 2 -Duration 3600
```

## PARAMETERS

### -Discard
Inform browsers to remove the cookie.

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

### -Duration
The duration, in seconds, before the cookie is expired.

```yaml
Type: Int32
Parameter Sets: Duration
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryDate
An explicit expiry date for the cookie.

```yaml
Type: DateTime
Parameter Sets: ExpiryDate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpOnly
Only allow the cookie to be used in browsers.

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

### -Name
The name of the cookie.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
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

### -Secret
If supplied, the secret with which to sign the cookie.

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
Only allow the cookie on secure (HTTPS) connections.

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

### -Value
The value of the cookie.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable
## NOTES

## RELATED LINKS
