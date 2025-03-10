---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# Get-PodeLimitRateRule

## SYNOPSIS
Gets a rate limit rule by name.

## SYNTAX

```
Get-PodeLimitRateRule [[-Name] <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Gets a rate limit rule by name.

## EXAMPLES

### EXAMPLE 1
```
$rules = Get-PodeLimitRateRule -Name 'rule1'
```

### EXAMPLE 2
```
$rules = Get-PodeLimitRateRule -Name 'rule1', 'rule2'
```

### EXAMPLE 3
```
$rules = Get-PodeLimitRateRule
```

## PARAMETERS

### -Name
The name(s) of the rate limit rule.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### A hashtable array containing the rate limit rule(s).
## NOTES

## RELATED LINKS
