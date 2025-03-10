---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Metrics
schema: 2.0.0
---

# Get-PodeServerActiveSignalMetric

## SYNOPSIS
Returns the count of active signals.

## SYNTAX

```
Get-PodeServerActiveSignalMetric [[-Type] <String>] [[-CountType] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns the count of all, processing, or queued active signals; for either server or client signals.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeServerActiveSignalMetric
```

### EXAMPLE 2
```
Get-PodeServerActiveSignalMetric -Type Client -CountType Queued
```

## PARAMETERS

### -CountType
The count type to return.
(Default: Total)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: Total
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

### -Type
The type of signal to return.
(Default: Total)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: Total
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
