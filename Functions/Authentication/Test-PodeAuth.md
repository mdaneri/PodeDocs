---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Test-PodeAuth

## SYNOPSIS
Test and invoke an Authentication method to verify a user.

## SYNTAX

```
Test-PodeAuth [-Name] <String> [-IgnoreSession] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Test and invoke an Authentication method to verify a user.
This will verify a user's credentials on the request.
When testing OAuth2 methods, the first attempt will trigger a redirect to the provider and $false will be returned.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeAuth -Name 'BasicAuth') { ... }
```

### EXAMPLE 2
```
if (Test-PodeAuth -Name 'FormAuth' -IgnoreSession) { ... }
```

## PARAMETERS

### -IgnoreSession
If supplied, authentication will be re-verified on each call even if a valid session exists on the request.

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
The Name of the Authentication method.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Boolean
## NOTES

## RELATED LINKS
