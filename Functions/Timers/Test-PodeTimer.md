---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Timers
schema: 2.0.0
---

# Test-PodeTimer

## SYNOPSIS
Tests whether the passed Timer exists.

## SYNTAX

```
Test-PodeTimer [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Tests whether the passed Timer exists by its name.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeTimer -Name TimerName) { }
```

## PARAMETERS

### -Name
The Name of the Timer.

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
