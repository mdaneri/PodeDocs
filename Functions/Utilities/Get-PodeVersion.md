---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Get-PodeVersion

## SYNOPSIS
Retrieves the version of the Pode module.

## SYNTAX

```
Get-PodeVersion [-Raw]
```

## DESCRIPTION
The \`Get-PodeVersion\` function checks the version of the Pode module as specified in the module manifest.
If the module version is **not** the placeholder value (\`'$version$'\`), it returns the actual version prefixed with \`'v'\`.
If the module version **is** the placeholder value, indicating the development branch, it returns \`"\[dev\]"\`.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeVersion
Returns the Pode module version, e.g., `'v1.2.3'` for release versions or `"[dev]"` if in development.
```

### EXAMPLE 2
```
Get-PodeVersion -Raw
Returns the raw version number, e.g., `'1.2.3'`, without the `'v'` prefix.
```

## PARAMETERS

### -Raw
If specified, the function returns only the raw module version without the \`'v'\` prefix.
By default, the function formats the version as \`'vX.Y.Z'\` unless the module is in development mode.

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

## INPUTS

## OUTPUTS

### System.String
### Returns a string representing the Pode module version in one of the following formats:
### - `"vX.Y.Z"` for a release version (e.g., `"v1.2.3"`).
### - `"[dev]"` for development versions.
## NOTES
- If the module version is a placeholder (\`'$version$'\`), the function assumes it's running from the development branch.

## RELATED LINKS
