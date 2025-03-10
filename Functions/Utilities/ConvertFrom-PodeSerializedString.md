---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# ConvertFrom-PodeSerializedString

## SYNOPSIS
Converts a serialized string back into its original data structure based on the specified serialization style.

## SYNTAX

```
ConvertFrom-PodeSerializedString [-SerializedInput] <String> [-Style <String>] [-Explode]
 [-ParameterName <String>] [-UrlDecode] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`ConvertFrom-PodeSerializedString\` function takes a serialized string and converts it back into its original data structure (e.g., hashtable, array).
The function requires the serialization style to be specified via the \`-Style\` parameter.
Supported styles are 'Simple', 'Label', 'Matrix', 'Query', 'Form', 'SpaceDelimited', 'PipeDelimited', and 'DeepObject'.
The function also accepts an optional \`-Explode\` switch to indicate whether the string uses exploded serialization.
The \`-ParameterName\` parameter can be used to specify the key name when processing certain styles, such as 'Matrix' and 'DeepObject'.

## EXAMPLES

### EXAMPLE 1
```
# Simple style, explode = true
$serialized = "name=value,anotherName=anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Simple' -Explode
Write-Output $result
```

### EXAMPLE 2
```
# Simple style, explode = false
$serialized = "name,value,anotherName,anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Simple'
Write-Output $result
```

### EXAMPLE 3
```
# Label style, explode = true
$serialized = ".name=value.anotherName=anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Label' -Explode
Write-Output $result
```

### EXAMPLE 4
```
# Label style, explode = false
$serialized = ".name,value,anotherName,anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Label'
Write-Output $result
```

### EXAMPLE 5
```
# Matrix style, explode = true
$serialized = ";name=value;anotherName=anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Matrix' -Explode
Write-Output $result
```

### EXAMPLE 6
```
# Matrix style, explode = false
$serialized = ";id=3,4,5"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Matrix' -ParameterName 'id'
Write-Output $result
```

### EXAMPLE 7
```
# Query style, explode = true
$serialized = "?name=value&anotherName=anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Query' -Explode
Write-Output $result
```

### EXAMPLE 8
```
# Query style, explode = false
$serialized = "?name,value,anotherName,anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Query'
Write-Output $result
```

### EXAMPLE 9
```
# Form style, explode = true
$serialized = "?name=value&anotherName=anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Form' -Explode
Write-Output $result
```

### EXAMPLE 10
```
# Form style, explode = false
$serialized = "?name,value,anotherName,anotherValue"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'Form'
Write-Output $result
```

### EXAMPLE 11
```
# SpaceDelimited style, explode = true
$serialized = "?id=3&id=4&id=5"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'SpaceDelimited' -Explode -ParameterName 'id'
Write-Output $result
```

### EXAMPLE 12
```
# SpaceDelimited style, explode = false
$serialized = "?id=3%204%205"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'SpaceDelimited' -ParameterName 'id'
Write-Output $result
```

### EXAMPLE 13
```
# PipeDelimited style, explode = true
$serialized = "?id=3&id=4&id=5"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'PipeDelimited' -Explode -ParameterName 'id'
Write-Output $result
```

### EXAMPLE 14
```
# PipeDelimited style, explode = false
$serialized = "?id=3|4|5"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'PipeDelimited' -ParameterName 'id'
Write-Output $result
```

### EXAMPLE 15
```
# DeepObject style
$serialized = "myId[role]=admin&myId[firstName]=Alex"
$result = ConvertFrom-PodeSerializedString -SerializedInput $serialized -Style 'DeepObject' -ParameterName 'myId'
Write-Output $result
```

## PARAMETERS

### -Explode
Indicates whether the string uses exploded serialization (\`-Explode\`) or not (omit \`-Explode\`).
This affects how arrays and objects are handled.

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

### -ParameterName
Specifies the key name to match when processing certain styles, such as 'Matrix' and 'DeepObject'.
The default is 'id'.

```yaml
Type: String
Parameter Sets: (All)
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

### -SerializedInput
The serialized string to be converted back into its original data structure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Style
The serialization style to use for deserialization.
Options are 'Simple', 'Label', 'Matrix', 'Query', 'Form', 'SpaceDelimited', 'PipeDelimited', and 'DeepObject'.
The default is 'Form'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Form
Accept pipeline input: False
Accept wildcard characters: False
```

### -UrlDecode
If specified, the function will decode the input string using URL decoding before processing it.
This is useful
for handling serialized inputs that include URL-encoded characters, such as \`%20\` for spaces.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
For more information on serialization styles, refer to:
- https://swagger.io/docs/specification/serialization/
- https://tools.ietf.org/html/rfc6570

## RELATED LINKS
