---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Protect-PodeValue

## SYNOPSIS
Resolves and protects a value by ensuring it defaults to a specified fallback and optionally parses it as an enum.

## SYNTAX

```
Protect-PodeValue [[-Value] <Object>] [[-Default] <Object>] [[-EnumType] <Type>] [-CaseSensitive]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Protect-PodeValue\` function ensures that a given value is resolved.
If the value is empty, a default value is used instead.
Additionally, the function can parse the resolved value as an enum type with optional case sensitivity.

## EXAMPLES

### EXAMPLE 1
```
# Example 1: Resolve a value with a default fallback
$resolved = Protect-PodeValue -Value $null -Default "Fallback"
Write-Output $resolved  # Output: Fallback
```

### EXAMPLE 2
```
# Example 2: Resolve and parse a value as a case-insensitive enum
$resolvedEnum = Protect-PodeValue -Value "red" -Default "Blue" -EnumType ([type][System.ConsoleColor])
Write-Output $resolvedEnum  # Output: Red
```

### EXAMPLE 3
```
# Example 3: Resolve and parse a value as a case-sensitive enum
$resolvedEnum = Protect-PodeValue -Value "red" -Default "Blue" -EnumType ([type][System.ConsoleColor]) -CaseSensitive
# Throws an error if "red" does not match an enum member exactly (case-sensitive).
```

## PARAMETERS

### -CaseSensitive
Specifies whether the enum parsing should be case-sensitive.
By default, parsing is case-insensitive.

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

### -Default
The default value to fall back to if the input value is empty.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnumType
The type of enum to parse the resolved value into.
If specified, the resolved value must be a valid enum member.

```yaml
Type: Type
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### -Value
The input value to be resolved.

```yaml
Type: Object
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

### [object]
### Returns the resolved value, either as the original value, the default value, or a parsed enum.
## NOTES
This function resolves values using \`Resolve-PodeValue\` and validates enums using \`\[enum\]::IsDefined\`.

## RELATED LINKS
