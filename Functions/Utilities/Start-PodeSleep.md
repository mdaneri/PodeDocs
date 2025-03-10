---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Start-PodeSleep

## SYNOPSIS
A function to pause execution for a specified duration.
This function should be used in Pode as replacement for Start-Sleep

## SYNTAX

### Seconds
```
Start-PodeSleep [[-Seconds] <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Milliseconds
```
Start-PodeSleep [[-Milliseconds] <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Duration
```
Start-PodeSleep [[-Duration] <TimeSpan>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Start-PodeSleep\` function pauses script execution for a given duration specified in seconds, milliseconds, or a TimeSpan.

## EXAMPLES

### EXAMPLE 1
```
Start-PodeSleep -Seconds 5
```

Pauses execution for 5 seconds.

## PARAMETERS

### -Duration
Specifies the duration to pause execution using a TimeSpan object.

```yaml
Type: TimeSpan
Parameter Sets: Duration
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Milliseconds
Specifies the duration to pause execution in milliseconds.

```yaml
Type: Int32
Parameter Sets: Milliseconds
Aliases:

Required: False
Position: 1
Default value: 0
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

### -Seconds
Specifies the duration to pause execution in seconds.
Default is 1 second.

```yaml
Type: Int32
Parameter Sets: Seconds
Aliases:

Required: False
Position: 1
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### None.
## NOTES
This function is useful for scenarios where tracking the remaining wait time visually is helpful.

## RELATED LINKS
