---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# ConvertTo-PodeSerializedString

## SYNOPSIS
Converts an object (hashtable or array) to a serialized string using a specified serialization style.

## SYNTAX

```
ConvertTo-PodeSerializedString [-InputObject] <PSObject[]> [-Style <String>] [-Explode] [-NoUrlEncode]
 [-ParameterName <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`ConvertTo-PodeSerializedString\` function takes a hashtable or array and converts it into a serialized string
according to the specified serialization style.
It supports various styles such as 'Simple', 'Label', 'Matrix',
'Form', 'SpaceDelimited', 'PipeDelimited', and 'DeepObject'.

By default, parameter names and values are URL-encoded to ensure safe inclusion in URLs.
You can disable URL encoding
by using the \`-NoUrlEncode\` switch.

An optional \`-Explode\` switch can be used to modify the serialization format for certain styles, altering how arrays
and objects are represented in the serialized string.

## EXAMPLES

### EXAMPLE 1
```
$item = @{
    name = 'value'
    anotherName = 'anotherValue'
}
$serialized = ConvertTo-PodeSerializedString -InputObject $item -Style 'Form'
Write-Output $serialized
```

# Output:
# ?id=name%2Cvalue%2CanotherName%2CanotherValue

### EXAMPLE 2
```
$item = @{
    name = 'value'
    anotherName = 'anotherValue'
}
$serializedExplode = ConvertTo-PodeSerializedString -InputObject $item -Style 'DeepObject' -Explode
Write-Output $serializedExplode
```

# Output:
# ?id\[name\]=value&id\[anotherName\]=anotherValue

### EXAMPLE 3
```
$array = @('3', '4', '5')
$serialized = ConvertTo-PodeSerializedString -InputObject $array -Style 'SpaceDelimited' -Explode
Write-Output $serialized
```

# Output:
# ?id=3&id=4&id=5

### EXAMPLE 4
```
$array = @('3', '4', '5')
$serialized = ConvertTo-PodeSerializedString -InputObject $array -Style 'SpaceDelimited' -NoUrlEncode
Write-Output $serialized
```

# Output:
# ?id=3 4 5

### EXAMPLE 5
```
$item = @{
    'user name' = 'Alice & Bob'
    'role' = 'Admin/User'
}
$serialized = ConvertTo-PodeSerializedString -InputObject $item -Style 'Form' -ParameterName 'account' -NoUrlEncode
Write-Output $serialized
```

# Output:
# ?account=user name,Alice & Bob,role,Admin/User

## PARAMETERS

### -Explode
An optional switch to modify the serialization format for certain styles.
When used, arrays and objects are
serialized in an expanded form.

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

### -InputObject
The object to be serialized.
This can be a hashtable (or ordered dictionary) or an array.
Supports pipeline input.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoUrlEncode
An optional switch to disable URL encoding of the serialized output.
By default, parameter names and values are
URL-encoded individually.
Use this switch if you require the output without URL encoding.

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
Specifies the name of the parameter to use in the serialized output.
Defaults to 'id' if not specified.

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

### -Style
The serialization style to use.
Valid values are 'Simple', 'Label', 'Matrix', 'Form', 'SpaceDelimited',
'PipeDelimited', and 'DeepObject'.
Defaults to 'Simple'.

```yaml
Type: String
Parameter Sets: (All)
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
- 'SpaceDelimited' and 'PipeDelimited' styles for hashtables are not implemented as they are not defined by RFC 6570.
- The 'Form' style with 'Explode' for arrays is not implemented for the same reason.
- The 'Explode' option for 'SpaceDelimited' and 'PipeDelimited' styles for arrays is implemented as per the OpenAPI Specification.

Additional information regarding serialization:
- OpenAPI Specification Serialization: https://swagger.io/docs/specification/serialization/
- RFC 6570 - URI Template: https://tools.ietf.org/html/rfc6570

## RELATED LINKS
