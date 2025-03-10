---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Schedules
schema: 2.0.0
---

# Edit-PodeSchedule

## SYNOPSIS
Edits an existing Schedule.

## SYNTAX

```
Edit-PodeSchedule [-Name] <String> [[-Cron] <String[]>] [[-ScriptBlock] <ScriptBlock>]
 [[-ArgumentList] <Hashtable>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Edits an existing Schedule's properties, such an cron expressions or scriptblock.

## EXAMPLES

### EXAMPLE 1
```
Edit-PodeSchedule -Name 'Hello' -Cron '@minutely'
```

### EXAMPLE 2
```
Edit-PodeSchedule -Name 'Hello' -Cron @('@hourly', '0 0 * * TUE')
```

## PARAMETERS

### -ArgumentList
Any new Arguments for the Schedule.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cron
Any new Cron Expressions for the Schedule.

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

### -ScriptBlock
The new ScriptBlock for the Schedule.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
