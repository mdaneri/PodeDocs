---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Security
schema: 2.0.0
---

# Remove-PodeSecurityHeader

## SYNOPSIS
Removes definition for specified security header.

## SYNTAX

```
Remove-PodeSecurityHeader [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Removes definition for specified security header.

## EXAMPLES

### EXAMPLE 1
```
Remove-PodeSecurityHeader -Name 'X-Header-Name'
```

## PARAMETERS

### -Name
The Name of the security header.

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

## NOTES

## RELATED LINKS
