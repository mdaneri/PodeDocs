---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Schedules
schema: 2.0.0
---

# Get-PodeScheduleNextTrigger

## SYNOPSIS
Get the next trigger time for a Schedule.

## SYNTAX

```
Get-PodeScheduleNextTrigger [-Name] <String> [[-DateTime] <Object>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Get the next trigger time for a Schedule, either from the Schedule's StartTime or from a defined DateTime.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeScheduleNextTrigger -Name Schedule1
```

### EXAMPLE 2
```
Get-PodeScheduleNextTrigger -Name Schedule1 -DateTime [datetime]::new(2020, 3, 10)
```

## PARAMETERS

### -DateTime
An optional specific DateTime to get the next trigger time after.
This DateTime must be between the Schedule's StartTime and EndTime.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Schedule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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
