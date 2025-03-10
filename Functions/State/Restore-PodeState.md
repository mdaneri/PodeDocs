---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: State
schema: 2.0.0
---

# Restore-PodeState

## SYNOPSIS
Restores the Pode shared state from a JSON file.

## SYNTAX

```
Restore-PodeState [-Path] <String> [-Merge] [[-Depth] <Int16>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This function reads a JSON file and restores the Pode server state.
It preserves dictionary types (ConcurrentDictionary, Hashtable, OrderedDictionary)
and ensures state integrity.
If the file does not exist, the function exits silently.

The function supports **merging** the restored state with the current Pode state or
**overwriting** it entirely.

## EXAMPLES

### EXAMPLE 1
```
Restore-PodeState -Path './state.json'
Restores the Pode state from `state.json`, replacing the current state.
```

### EXAMPLE 2
```
Restore-PodeState -Path './state.json' -Merge
Merges the loaded state with the existing Pode state.
```

## PARAMETERS

### -Depth
Defines the maximum depth for JSON deserialization.
This value is passed to \`ConvertFrom-PodeCustomDictionaryJson\`.
Default is **20**.

```yaml
Type: Int16
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### -Merge
If specified, the loaded state will be merged with the existing Pode state instead
of replacing it.

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

### -Path
Specifies the JSON file path containing the saved state.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### [System.Void] - The function updates `$PodeContext.Server.State` but does not return a value.
## NOTES
- This function is intended for internal Pode usage and may be subject to changes.
- For more details, refer to: https://github.com/Badgerati/Pode/tree/develop

## RELATED LINKS
