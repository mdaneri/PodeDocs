---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Caching
schema: 2.0.0
---

# Set-PodeCache

## SYNOPSIS
Set (create/update) a key in the cache.
You can use "$cache:key = 'value'" as well.

## SYNTAX

```
Set-PodeCache -Key <String> [-InputObject] <Object> [-Ttl <Int32>] [-Storage <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Set (create/update) a key in the cache, with an optional TTL value.
You can use "$cache:key = 'value'" as well.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeCache -Key 'ExampleKey' -InputObject 'ExampleValue'
```

### EXAMPLE 2
```
Set-PodeCache -Key 'ExampleKey' -InputObject 'ExampleValue' -Storage 'ExampleStorage'
```

### EXAMPLE 3
```
Set-PodeCache -Key 'ExampleKey' -InputObject 'ExampleValue' -Ttl 300
```

### EXAMPLE 4
```
Set-PodeCache -Key 'ExampleKey' -InputObject @{ Value = 'ExampleValue' }
```

### EXAMPLE 5
```
@{ Value = 'ExampleValue' } | Set-PodeCache -Key 'ExampleKey'
```

### EXAMPLE 6
```
$cache:ExampleKey = 'ExampleValue'
```

## PARAMETERS

### -InputObject
The value of the key to be set, can be any object type.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Key
The Key to be set.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

### -Storage
An optional cache Storage name.
(Default: in-memory)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
An optional TTL value, in seconds.
The default is whatever "Get-PodeCacheDefaultTtl" retuns, which will be 3600 seconds when not set.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
