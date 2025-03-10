---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Schedules
schema: 2.0.0
---

# Invoke-PodeSchedule

## SYNOPSIS
Adhoc invoke a Schedule's logic.

## SYNTAX

```
Invoke-PodeSchedule [-Name] <String> [[-ArgumentList] <Hashtable>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Adhoc invoke a Schedule's logic outside of its defined cron-expression.
This invocation doesn't count towards the Schedule's limit.

## EXAMPLES

### EXAMPLE 1
```
Invoke-PodeSchedule -Name 'schedule-name'
```

## PARAMETERS

### -ArgumentList
A hashtable of arguments to supply to the Schedule's ScriptBlock.

```yaml
Type: Hashtable
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
