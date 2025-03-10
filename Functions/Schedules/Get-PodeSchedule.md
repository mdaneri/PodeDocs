---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Schedules
schema: 2.0.0
---

# Get-PodeSchedule

## SYNOPSIS
Returns any defined schedules.

## SYNTAX

```
Get-PodeSchedule [[-Name] <String[]>] [[-StartTime] <Object>] [[-EndTime] <Object>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns any defined schedules, with support for filtering.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeSchedule
```

### EXAMPLE 2
```
Get-PodeSchedule -Name Name1, Name2
```

### EXAMPLE 3
```
Get-PodeSchedule -Name Name1, Name2 -StartTime [datetime]::new(2020, 3, 1) -EndTime [datetime]::new(2020, 3, 31)
```

## PARAMETERS

### -EndTime
An optional EndTime to only return Schedules that will trigger before this date.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Any schedule Names to filter the schedules.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -StartTime
An optional StartTime to only return Schedules that will trigger after this date.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
