---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Test-PodeIsEmpty

## SYNOPSIS
Tests if a value is empty - the value can be of any type.

## SYNTAX

```
Test-PodeIsEmpty [[-Value] <Object>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Tests if a value is empty - the value can be of any type.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeIsEmpty @{}) { /* logic */ }
```

## PARAMETERS

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

### -Value
The value to test.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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
