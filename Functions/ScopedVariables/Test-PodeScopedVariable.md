---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: ScopedVariables
schema: 2.0.0
---

# Test-PodeScopedVariable

## SYNOPSIS
Tests if a Scoped Variable exists.

## SYNTAX

```
Test-PodeScopedVariable [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Tests if a Scoped Variable exists.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeScopedVariable -Name $Name) { ... }
```

## PARAMETERS

### -Name
The Name of the Scoped Variable to check.

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
