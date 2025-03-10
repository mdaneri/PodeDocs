---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: State
schema: 2.0.0
---

# Save-PodeState

## SYNOPSIS
Saves the current Pode server state to a JSON file.

## SYNTAX

```
Save-PodeState [-Path] <String> [[-Scope] <String[]>] [[-Exclude] <String[]>] [[-Include] <String[]>]
 [[-Depth] <Int16>] [-Compress] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function serializes the Pode state into a JSON file while preserving the structure
of dictionaries (\`ConcurrentDictionary\`, \`Hashtable\`, \`OrderedDictionary\`).
It allows
filtering the saved state by scope, inclusion, or exclusion of specific keys.

For thread safety, it is recommended to wrap this function inside a \`Lock-PodeObject\` block.

## EXAMPLES

### EXAMPLE 1
```
Save-PodeState -Path './state.json'
Saves the entire Pode state to `state.json`.
```

### EXAMPLE 2
```
Save-PodeState -Path './state.json' -Exclude 'SessionData', 'UserCache'
Saves the Pode state but **excludes** the specified state keys.
```

### EXAMPLE 3
```
Save-PodeState -Path './state.json' -Scope 'Users'
Saves **only** state objects that belong to the `"Users"` scope.
```

## PARAMETERS

### -Compress
If specified, the JSON output will be minified (no extra whitespace).

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

### -Depth
Defines the maximum depth for JSON serialization.
This value is passed to \`ConvertTo-PodeCustomDictionaryJson\`.
Default is **20**.

```yaml
Type: Int16
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exclude
Specifies state object names to **exclude** from being saved.
This filter has **higher precedence** than Include.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Include
Specifies state object names to **only** include in the saved state.
This filter has **lower precedence** than Exclude.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the file path where the state should be saved.

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

### -Scope
Filters the state objects to be saved based on their scope.
Only state objects within the specified scope(s) will be included.
This filter has **lower precedence** than Exclude and Include.

```yaml
Type: String[]
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

### [System.Void] - This function does not return an output. The state is saved to a file.
## NOTES
- This function is intended for internal Pode usage and may be subject to changes.
- For more information, refer to: https://github.com/Badgerati/Pode/tree/develop

## RELATED LINKS
