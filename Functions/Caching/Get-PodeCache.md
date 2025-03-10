---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Caching
schema: 2.0.0
---

# Get-PodeCache

## SYNOPSIS
Return the value of a key from the cache.
You can use "$value = $cache:key" as well.

## SYNTAX

```
Get-PodeCache [-Key] <String> [[-Storage] <String>] [-Metadata] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Return the value of a key from the cache, or returns the value plus metadata such as expiry time if required.
You can use "$value = $cache:key" as well.

## EXAMPLES

### EXAMPLE 1
```
$value = Get-PodeCache -Key 'ExampleKey'
```

### EXAMPLE 2
```
$value = Get-PodeCache -Key 'ExampleKey' -Storage 'ExampleStorage'
```

### EXAMPLE 3
```
$value = Get-PodeCache -Key 'ExampleKey' -Metadata
```

### EXAMPLE 4
```
$value = $cache:ExampleKey
```

## PARAMETERS

### -Key
The Key to be retrieved.

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

### -Metadata
If supplied, and if supported by the cache storage, an metadata such as expiry times will also be returned.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
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
Position: 2
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
