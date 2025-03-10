---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# New-PodeAuthTwitterScheme

## SYNOPSIS
Create an OAuth2 auth scheme for Twitter.

## SYNTAX

```
New-PodeAuthTwitterScheme [-ClientId] <String> [[-ClientSecret] <String>] [[-RedirectUrl] <String>]
 [[-Middleware] <Object[]>] [-UsePKCE] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
A wrapper for New-PodeAuthScheme and OAuth2, which builds an OAuth2 scheme for Twitter apps.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAuthTwitterScheme -ClientId some_id -ClientSecret 1234.abc
```

### EXAMPLE 2
```
New-PodeAuthTwitterScheme -ClientId some_id -UsePKCE
```

## PARAMETERS

### -ClientId
The Client ID from registering a new app.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientSecret
The Client Secret from registering a new app (this is optional when using PKCE).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Middleware
An array of ScriptBlocks for optional Middleware to run before the Scheme's scriptblock.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -RedirectUrl
An optional OAuth2 Redirect URL (default: \<host\>/oauth2/callback)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePKCE
If supplied, OAuth2 authentication will use PKCE code verifiers.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable
## NOTES

## RELATED LINKS
