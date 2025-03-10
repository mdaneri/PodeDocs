---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Get-PodeQueryParameter

## SYNOPSIS
Retrieves a specific query parameter value from the current Pode web event.

## SYNTAX

### BuiltIn (Default)
```
Get-PodeQueryParameter -Name <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Deserialize
```
Get-PodeQueryParameter -Name <String> [-Deserialize] [-NoExplode] [-Style <String>] [-ParameterName <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Get-PodeQueryParameter\` function extracts and returns the value of a specified query parameter
from the current Pode web event.
This function is designed to access query parameters passed in the URL of a web request,
enabling the handling of incoming data in web applications.

The function supports deserialization of query parameter values when the \`-Deserialize\` switch is used,
allowing for interpretation of complex data structures from the query string.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeQueryParameter -Name 'userId'
Returns the value of the 'userId' query parameter from the current web event.
```

### EXAMPLE 2
```
Get-PodeQueryParameter -Name 'filter' -Deserialize -Style 'SpaceDelimited'
Retrieves and deserializes the value of the 'filter' query parameter, using the 'SpaceDelimited' style.
```

### EXAMPLE 3
```
Get-PodeQueryParameter -Name 'data' -Deserialize -NoExplode
Deserializes the 'data' query parameter value without exploding arrays.
```

## PARAMETERS

### -Deserialize
Specifies that the query parameter value should be deserialized.
When this switch is used, the value will be
interpreted based on the provided style and other deserialization options.

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

### -Name
The name of the query parameter to retrieve.
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

### -NoExplode
Prevents deserialization from exploding arrays in the query parameter value.
This is useful when handling
parameters that contain comma-separated values and when array expansion is not desired.
Applicable only when
the \`-Deserialize\` switch is used.

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
Specifies the key name to use when deserializing the query parameter value.
The default value is 'id'.
This option is useful for mapping the query parameter data accurately during deserialization.
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
Defines the deserialization style to use when interpreting the query parameter value.
Valid options are 'Simple',
'Label', 'Matrix', 'Form', 'SpaceDelimited', 'PipeDelimited', and 'DeepObject'.
The default is 'Form'.
Applicable only when the \`-Deserialize\` switch is used.

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
advanced handling of complex query parameter data structures.

## RELATED LINKS
