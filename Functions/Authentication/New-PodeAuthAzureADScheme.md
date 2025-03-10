---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# New-PodeAuthAzureADScheme

## SYNOPSIS
Create an OAuth2 auth scheme for Azure AD.

## SYNTAX

```
New-PodeAuthAzureADScheme [[-Tenant] <String>] [-ClientId] <String> [[-ClientSecret] <String>]
 [[-RedirectUrl] <String>] [[-InnerScheme] <Hashtable>] [[-Middleware] <Object[]>] [-UsePKCE]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
A wrapper for New-PodeAuthScheme and OAuth2, which builds an OAuth2 scheme for Azure AD.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAuthAzureADScheme -Tenant 123-456-678 -ClientId some_id -ClientSecret 1234.abc
```

### EXAMPLE 2
```
New-PodeAuthAzureADScheme -Tenant 123-456-678 -ClientId some_id -UsePKCE
```

## PARAMETERS

### -ClientId
The Client ID from registering a new app.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InnerScheme
An optional authentication Scheme (from New-PodeAuthScheme) that will be called prior to this Scheme.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Middleware
An array of ScriptBlocks for optional Middleware to run before the Scheme's scriptblock.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
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
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
The Directory/Tenant ID from registering a new app (default: common).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: Common
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
