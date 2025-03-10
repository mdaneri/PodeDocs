---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Schedules
schema: 2.0.0
---

# Add-PodeSchedule

## SYNOPSIS
Adds a new Schedule with logic to periodically invoke, defined using Cron Expressions.

## SYNTAX

### Script (Default)
```
Add-PodeSchedule -Name <String> -Cron <String[]> -ScriptBlock <ScriptBlock> [-Limit <Int32>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-ArgumentList <Hashtable>] [-Timeout <Int32>]
 [-TimeoutFrom <String>] [-OnStart] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodeSchedule -Name <String> -Cron <String[]> [-Limit <Int32>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 -FilePath <String> [-ArgumentList <Hashtable>] [-Timeout <Int32>] [-TimeoutFrom <String>] [-OnStart]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a new Schedule with logic to periodically invoke, defined using Cron Expressions.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeSchedule -Name 'RunEveryMinute' -Cron '@minutely' -ScriptBlock { /* logic */ }
```

### EXAMPLE 2
```
Add-PodeSchedule -Name 'RunEveryTuesday' -Cron '0 0 * * TUE' -ScriptBlock { /* logic */ }
```

### EXAMPLE 3
```
Add-PodeSchedule -Name 'StartAfter2days' -Cron '@hourly' -StartTime [DateTime]::Now.AddDays(2) -ScriptBlock { /* logic */ }
```

### EXAMPLE 4
```
Add-PodeSchedule -Name 'Args' -Cron '@minutely' -ScriptBlock { /* logic */ } -ArgumentList @{ Arg1 = 'value' }
```

## PARAMETERS

### -ArgumentList
A hashtable of arguments to supply to the Schedule's ScriptBlock.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cron
One, or an Array, of Cron Expressions to define when the Schedule should trigger.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
A DateTime for when the Schedule should stop triggering, and be removed.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the Schedule's logic.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit
The number of times the Schedule should trigger before being removed.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnStart
If supplied, the schedule will trigger when the server starts, regardless if the cron-expression matches the current time.

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

### -ScriptBlock
The script defining the Schedule's logic.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
A DateTime for when the Schedule should start triggering.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
An optional timeout, in seconds, for the Schedule's logic.
(Default: -1 \[never timeout\])

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeoutFrom
An optional timeout from either 'Create' or 'Start'.
(Default: 'Create')

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Create
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
