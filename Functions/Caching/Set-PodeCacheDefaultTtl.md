---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Caching
schema: 2.0.0
---

# Set-PodeCacheDefaultTtl

## SYNOPSIS
Set a default cache TTL.

## SYNTAX

```
Set-PodeCacheDefaultTtl [-Value] <Int32> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Set a default cache TTL.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeCacheDefaultTtl -Value 3600
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

### -Value
A default TTL value, in seconds, to use when setting cache key expiries.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
