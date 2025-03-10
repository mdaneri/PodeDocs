---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Caching
schema: 2.0.0
---

# Clear-PodeCache

## SYNOPSIS
Clear all keys from the cache.

## SYNTAX

```
Clear-PodeCache [[-Storage] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Clear all keys from the cache.

## EXAMPLES

### EXAMPLE 1
```
Clear-PodeCache
```

### EXAMPLE 2
```
Clear-PodeCache -Storage 'ExampleStorage'
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

### -Storage
An optional cache Storage name.
(Default: in-memory)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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
