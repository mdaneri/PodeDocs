---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Caching
schema: 2.0.0
---

# Add-PodeCacheStorage

## SYNOPSIS
Add a cache storage.

## SYNTAX

```
Add-PodeCacheStorage [-Name] <String> [-Get] <ScriptBlock> [-Set] <ScriptBlock> [-Remove] <ScriptBlock>
 [-Test] <ScriptBlock> [-Clear] <ScriptBlock> [-Default] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Add a cache storage.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeCacheStorage -Name 'ExampleStorage' -Get {} -Set {} -Remove {} -Test {} -Clear {}
```

## PARAMETERS

### -Clear
A Clear ScriptBlock, to remove all keys from the cache.
Use an empty ScriptBlock if not supported.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Default
If supplied, this cache storage will be set as the default storage.

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

### -Get
A Get ScriptBlock, to retrieve a key's value from the cache, or the value plus metadata if required.
Supplied parameters: Key, Metadata.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the cache storage.

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

### -Remove
A Remove ScriptBlock, to remove a key from the cache.
Supplied parameters: Key.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Set
A Set ScriptBlock, to set/create/update a key's value in the cache.
Supplied parameters: Key, Value, TTL.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Test
A Test ScriptBlock, to test if a key exists in the cache.
Supplied parameters: Key.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
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
