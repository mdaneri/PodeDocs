---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: State
schema: 2.0.0
---

# Set-PodeState

## SYNOPSIS
Sets an object within the shared state.

## SYNTAX

### Value (Default)
```
Set-PodeState -Name <String> [[-Value] <Object>] [-Scope <String[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Collection
```
Set-PodeState -Name <String> [-Scope <String[]>] -NewCollectionType <String>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Sets an object within the shared state, allowing for the creation of different collection types, such as a Hashtable, ConcurrentDictionary, or other concurrent collections.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeState -Name 'Data' -Value @{ 'Name' = 'Rick Sanchez' }
```

### EXAMPLE 2
```
Set-PodeState -Name 'Users' -Value @('user1', 'user2') -Scope General, Users
```

### EXAMPLE 3
```
Set-PodeState -Name 'Cache' -NewCollectionType 'ConcurrentDictionary'
```

### EXAMPLE 4
```
Set-PodeState -Name 'Tasks' -NewCollectionType 'ConcurrentQueue'
```

## PARAMETERS

### -Name
The name of the state object.

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

### -NewCollectionType
Specifies the type of collection to create.
Supported options include:
- Hashtable
- ConcurrentDictionary
- OrderedDictionary
- ConcurrentBag
- ConcurrentQueue
- ConcurrentStack

If this parameter is used, the state object will be initialized as the specified collection type.

```yaml
Type: String
Parameter Sets: Collection
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

### -Scope
An optional scope for the state object, used when saving the state.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
The value to set in the state.
If a collection type is specified using \`-NewCollectionType\`, this value is ignored.

```yaml
Type: Object
Parameter Sets: Value
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object
## NOTES
- \`NewCollectionType\` and \`Value\` are mutually exclusive; only one can be used at a time.
- The function ensures thread safety when using concurrent collections.
- Pode must be initialized before calling this function.

## RELATED LINKS
