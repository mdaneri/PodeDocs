---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# New-PodeCron

## SYNOPSIS
A helper function to generate cron expressions.

## SYNTAX

```
New-PodeCron [[-Minute] <Int32[]>] [[-Hour] <Int32[]>] [[-Date] <Int32[]>] [[-Month] <String[]>]
 [[-Day] <String[]>] [[-Every] <String>] [[-Interval] <Int32>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
A helper function to generate cron expressions, which can be used for Schedules and other functions that use cron expressions.
This helper function only covers simple cron use-cases, with some advanced use-cases.
If you need further advanced cron
expressions it would be best to write the expression by hand.

## EXAMPLES

### EXAMPLE 1
```
New-PodeCron -Every Day                                             # every 00:00
```

### EXAMPLE 2
```
New-PodeCron -Every Day -Day Tuesday, Friday -Hour 1                # every tuesday and friday at 01:00
```

### EXAMPLE 3
```
New-PodeCron -Every Month -Date 15                                  # every 15th of the month at 00:00
```

### EXAMPLE 4
```
New-PodeCron -Every Date -Interval 2 -Date 2                        # every month, every other day from 2nd, at 00:00
```

### EXAMPLE 5
```
New-PodeCron -Every Year -Month June                                # every 1st june, at 00:00
```

### EXAMPLE 6
```
New-PodeCron -Every Hour -Hour 1 -Interval 1                        # every hour, starting at 01:00
```

### EXAMPLE 7
```
New-PodeCron -Every Minute -Hour 1, 2, 3, 4, 5 -Interval 15         # every 15mins, starting at 01:00 until 05:00
```

### EXAMPLE 8
```
New-PodeCron -Every Hour -Day Monday                                # every hour of every monday
```

### EXAMPLE 9
```
New-PodeCron -Every Quarter                                         # every 1st jan, apr, jul, oct, at 00:00
```

## PARAMETERS

### -Date
This is an array of Dates in the monnth that the expression should use between 1-31.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Day
This is an array of Days in the week that the expression should use between Monday-Sunday.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Every
This can be used to more easily specify "Every Hour" than writing out all the hours.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hour
This is an array of Hours that the expression should use between 0-23.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Interval
This can only be used when using the Every parameter, and will setup an interval on the "every" used.
If you want "every 2 hours" then Every should be set to Hour and Interval to 2.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Minute
This is an array of Minutes that the expression should use between 0-59.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Month
This is an array of Months that the expression should use between January-December.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### System.String
## NOTES

## RELATED LINKS
