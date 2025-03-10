---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# Update-PodeLimitRateRule

## SYNOPSIS
Updates a rate limit rule.

## SYNTAX

```
Update-PodeLimitRateRule [-Name] <String> [[-Limit] <Int32>] [[-Duration] <Int32>] [[-StatusCode] <Int32>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Updates a rate limit rule.

## EXAMPLES

### EXAMPLE 1
```
Update-PodeLimitRateRule -Name 'rule1' -Limit 10
```

### EXAMPLE 2
```
Update-PodeLimitRateRule -Name 'rule1' -Duration 10000
```

### EXAMPLE 3
```
Update-PodeLimitRateRule -Name 'rule1' -StatusCode 429
```

### EXAMPLE 4
```
Update-PodeLimitRateRule -Name 'rule1' -Limit 10 -Duration 10000 -StatusCode 429
```

## PARAMETERS

### -Duration
The new duration for the rule, in milliseconds.
If not supplied, the duration will not be updated.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit
The new limit for the rule.
If not supplied, the limit will not be updated.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the rate limit rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -StatusCode
The new status code for the rule.
If not supplied, the status code will not be updated.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
