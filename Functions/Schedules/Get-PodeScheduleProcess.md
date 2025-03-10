---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Schedules
schema: 2.0.0
---

# Get-PodeScheduleProcess

## SYNOPSIS
Get all Schedule Processes.

## SYNTAX

```
Get-PodeScheduleProcess [[-Name] <String[]>] [[-Id] <String[]>] [[-State] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Get all Schedule Processes, with support for filtering.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeScheduleProcess
```

### EXAMPLE 2
```
Get-PodeScheduleProcess -Name 'ScheduleName'
```

### EXAMPLE 3
```
Get-PodeScheduleProcess -Id 'ScheduleId'
```

### EXAMPLE 4
```
Get-PodeScheduleProcess -State 'Running'
```

## PARAMETERS

### -Id
An optional ID of the Schedule process to filter by, can be one or more.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
An optional Name of the Schedule to filter by, can be one or more.

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

### -State
An optional State of the Schedule process to filter by, can be one or more.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: All
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
