---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Get-PodeBodyData

## SYNOPSIS
Retrieves the body data from the current Pode web event.

## SYNTAX

### BuiltIn (Default)
```
Get-PodeBodyData [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Deserialize
```
Get-PodeBodyData [-Deserialize] [-NoExplode] [-Style <String>] [-ParameterName <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Get-PodeBodyData\` function extracts and returns the body data of the current Pode web event.
This function is designed to access the main content sent in web requests, including methods such as PUT, POST, or any other HTTP methods that support a request body.
It also supports deserialization of the body data, allowing for the interpretation of serialized content.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeBodyData
Returns the body data of the current web event.
```

### EXAMPLE 2
```
Get-PodeBodyData -Deserialize -Style 'Matrix'
Retrieves and deserializes the body data using the 'Matrix' style.
```

### EXAMPLE 3
```
Get-PodeBodyData -Deserialize -NoExplode
Deserializes the body data without exploding arrays.
```

## PARAMETERS

### -Deserialize
Specifies that the body data should be deserialized.
When this switch is used, the body data will be interpreted
based on the provided style and other deserialization options.

```yaml
Type: SwitchParameter
Parameter Sets: Deserialize
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExplode
Prevents deserialization from exploding arrays in the body data.
This is useful when handling parameters that
contain comma-separated values and when array expansion is not desired.
Applicable only when the \`-Deserialize\`
switch is used.

```yaml
Type: SwitchParameter
Parameter Sets: Deserialize
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParameterName
Specifies the key name to use when deserializing the body data.
The default value is 'id'.
This option is useful
for mapping the body data accurately during deserialization.
Applicable only when the \`-Deserialize\` switch is used.

```yaml
Type: String
Parameter Sets: Deserialize
Aliases:

Required: False
Position: Named
Default value: Id
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

### -Style
Defines the deserialization style to use when interpreting the body data.
Valid options are 'Simple', 'Label',
'Matrix', 'Form', 'SpaceDelimited', 'PipeDelimited', and 'DeepObject'.
The default is 'Form'.
Applicable only
when the \`-Deserialize\` switch is used.

```yaml
Type: String
Parameter Sets: Deserialize
Aliases:

Required: False
Position: Named
Default value: Form
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
This function should be used within a route's script block in a Pode server.
The \`-Deserialize\` switch enables
advanced handling of complex body data structures.

## RELATED LINKS
