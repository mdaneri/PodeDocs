---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Test-PodeAuthUser

## SYNOPSIS
Test whether the current WebEvent or Session has an authenticated user.

## SYNTAX

```
Test-PodeAuthUser [-IgnoreSession] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Test whether the current WebEvent or Session has an authenticated user.
Returns true if there is an authenticated user.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeAuthUser) { ... }
```

## PARAMETERS

### -IgnoreSession
If supplied, only the Auth object in the WebEvent will be checked and the Session will be skipped.

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
