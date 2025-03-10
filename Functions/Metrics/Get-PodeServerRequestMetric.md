---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Metrics
schema: 2.0.0
---

# Get-PodeServerRequestMetric

## SYNOPSIS
Returns the total number of requests/per status code the Server has receieved.

## SYNTAX

### StatusCode (Default)
```
Get-PodeServerRequestMetric [-StatusCode <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Total
```
Get-PodeServerRequestMetric [-Total] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns the total number of requests/per status code the Server has receieved.

## EXAMPLES

### EXAMPLE 1
```
$totalReqs = Get-PodeServerRequestMetric -Total
```

### EXAMPLE 2
```
$statusReqs = Get-PodeServerRequestMetric
```

### EXAMPLE 3
```
$404Reqs = Get-PodeServerRequestMetric -StatusCode 404
```

## PARAMETERS

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

### -StatusCode
If supplied, will return the total number of requests for a specific StatusCode.

```yaml
Type: Int32
Parameter Sets: StatusCode
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Total
If supplied, will return the Total number of Requests.

```yaml
Type: SwitchParameter
Parameter Sets: Total
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Int64
## NOTES

## RELATED LINKS
