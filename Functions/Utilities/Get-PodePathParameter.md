---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Get-PodePathParameter

## SYNOPSIS
Retrieves a specific parameter value from the current Pode web event.

## SYNTAX

### BuiltIn (Default)
```
Get-PodePathParameter -Name <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Deserialize
```
Get-PodePathParameter -Name <String> [-Deserialize] [-Explode] [-Style <String>] [-ParameterName <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Get-PodePathParameter\` function extracts and returns the value of a specified parameter
from the current Pode web event.
This function can access parameters passed in the URL path, query string,
or body of a web request, making it useful in web applications to dynamically handle incoming data.

The function supports deserialization of parameter values when the \`-Deserialize\` switch is used.
This allows for interpreting serialized data structures, like arrays or complex objects, from the web request.

## EXAMPLES

### EXAMPLE 1
```
Get-PodePathParameter -Name 'action'
Returns the value of the 'action' parameter from the current web event.
```

### EXAMPLE 2
```
Get-PodePathParameter -Name 'item' -Deserialize -Style 'Label' -Explode
Retrieves and deserializes the value of the 'item' parameter using the 'Label' style and exploding arrays.
```

### EXAMPLE 3
```
Get-PodePathParameter -Name 'id' -Deserialize -KeyName 'userId'
Deserializes the 'id' parameter using the key name 'userId'.
```

## PARAMETERS

### -Deserialize
Specifies that the parameter value should be deserialized.
When this switch is used, the value will be interpreted
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

### -Explode
Specifies whether to explode arrays when deserializing the parameter value.
This is useful when parameters contain
comma-separated values.
Applicable only when the \`-Deserialize\` switch is used.

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

### -Name
The name of the parameter to retrieve.
This parameter is mandatory.

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

### -ParameterName
Specifies the key name to use when deserializing the parameter value.
The default value is 'id'.
This option is useful for mapping the parameter data accurately during deserialization.
Applicable only
when the \`-Deserialize\` switch is used.

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
Defines the deserialization style to use when interpreting the parameter value.
Valid options are 'Simple', 'Label',
and 'Matrix'.
The default is 'Simple'.
Applicable only when the \`-Deserialize\` switch is used.

```yaml
Type: String
Parameter Sets: Deserialize
Aliases:

Required: False
Position: Named
Default value: Simple
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
This function should be used within a route's script block in a Pode server.
The \`-Deserialize\` switch enables more advanced handling of complex data structures.

## RELATED LINKS
