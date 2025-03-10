---
external help file: Pode-help.xml
Module Name: Pode
online version: https://swagger.io/docs/specification/basic-structure/
PodeType: OAProperties
schema: 2.0.0
---

# New-PodeOAIntProperty

## SYNOPSIS
Creates a new OpenAPI integer property.

## SYNTAX

### Inbuilt (Default)
```
New-PodeOAIntProperty [[-ParamsList] <Hashtable[]>] [-Name <String>] [-Format <String>] [-Default <Int32>]
 [-Minimum <Int32>] [-Maximum <Int32>] [-ExclusiveMaximum] [-ExclusiveMinimum] [-MultiplesOf <Int32>]
 [-Description <String>] [-ExternalDoc <String>] [-Example <Object>] [-Enum <Int32[]>] [-Required]
 [-Deprecated] [-Object] [-Nullable] [-ReadOnly] [-WriteOnly] [-NoAdditionalProperties]
 [-AdditionalProperties <Hashtable>] [-XmlName <String>] [-XmlNamespace <String>] [-XmlPrefix <String>]
 [-XmlAttribute] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Array
```
New-PodeOAIntProperty [[-ParamsList] <Hashtable[]>] [-Name <String>] [-Format <String>] [-Default <Int32>]
 [-Minimum <Int32>] [-Maximum <Int32>] [-ExclusiveMaximum] [-ExclusiveMinimum] [-MultiplesOf <Int32>]
 [-Description <String>] [-ExternalDoc <String>] [-Example <Object>] [-Enum <Int32[]>] [-Required]
 [-Deprecated] [-Object] [-Nullable] [-ReadOnly] [-WriteOnly] [-NoAdditionalProperties]
 [-AdditionalProperties <Hashtable>] [-XmlName <String>] [-XmlNamespace <String>] [-XmlPrefix <String>]
 [-XmlAttribute] [-XmlItemName <String>] [-XmlWrapped] [-Array] [-UniqueItems] [-MinItems <Int32>]
 [-MaxItems <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new OpenAPI integer property, for Schemas or Parameters.

## EXAMPLES

### EXAMPLE 1
```
New-PodeOAIntProperty -Name 'age' -Required
Creates a required integer property named 'age'.
```

### EXAMPLE 2
```
New-PodeOAIntProperty -Name 'count' -Minimum 0 -Maximum 10 -Default 5 -Description 'Item count'
Creates an integer property 'count' with a minimum value of 0, maximum of 10, default value of 5, and a description.
```

### EXAMPLE 3
```
New-PodeOAIntProperty -Name 'quantity' -XmlName 'Quantity' -XmlNamespace 'http://example.com/quantity' -XmlPrefix 'q'
Creates an integer property 'quantity' with a custom XML element name 'Quantity', using a specified namespace and prefix.
```

### EXAMPLE 4
```
New-PodeOAIntProperty -Array -XmlItemName 'unit' -XmlName 'units' | Add-PodeOAComponentSchema -Name 'Units'
Generates a schema where the integer property is treated as an array, with each array item named 'unit' in XML, and the array itself represented with the XML name 'units'.
```

## PARAMETERS

### -AdditionalProperties
Define a set of additional properties for the OpenAPI schema.
This parameter accepts a HashTable where each key-value pair represents a property name and its corresponding schema.
The schema for each property can include type, format, description, and other OpenAPI specification attributes.
When specified, these additional properties are included in the OpenAPI definition, allowing for more flexible and dynamic object structures.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Array
If supplied, the object will be treated as an array of objects.

```yaml
Type: SwitchParameter
Parameter Sets: Array
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Default
The default value of the property.
(Default: 0)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Deprecated
If supplied, the object will be treated as Deprecated where supported.

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

### -Description
A Description of the property.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enum
An optional array of values that this property can only be set to.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Example
An example of a parameter value

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExclusiveMaximum
Specifies an exclusive upper limit for a numeric property in the OpenAPI schema.
When this parameter is used, it sets the exclusiveMaximum attribute in the OpenAPI definition to true, indicating that the numeric value must be strictly less than the specified maximum value.
This parameter is typically paired with a -Maximum parameter to define the upper bound.

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

### -ExclusiveMinimum
Specifies an exclusive lower limit for a numeric property in the OpenAPI schema.
When this parameter is used, it sets the exclusiveMinimun attribute in the OpenAPI definition to true, indicating that the numeric value must be strictly less than the specified minimun value.
This parameter is typically paired with a -Minimum parameter to define the lower bound.

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

### -ExternalDoc
If supplied, add an additional external documentation for this operation.
The parameter is created by Add-PodeOAExternalDoc

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Format
The inbuilt OpenAPI Format of the integer.
(Default: Any)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Maximum
The maximum value of the integer.
(Default: Int.Max)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxItems
If supplied, specify maximum length of an array

```yaml
Type: Int32
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Minimum
The minimum value of the integer.
(Default: Int.Min)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinItems
If supplied, specify minimum length of an array

```yaml
Type: Int32
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -MultiplesOf
The integer must be in multiples of the supplied value.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the property.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Title

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoAdditionalProperties
If supplied, will configure the OpenAPI property additionalProperties to false.
This means that the defined object will not allow any properties beyond those explicitly declared in its schema.
If any additional properties are provided, they will be considered invalid.
Use this switch to enforce a strict schema definition, ensuring that objects contain only the specified set of properties and no others.

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

### -Nullable
If supplied, the integer will be treated as Nullable.

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

### -Object
If supplied, the integer will be automatically wrapped in an object.

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

### -ParamsList
Used to pipeline multiple properties

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### -ReadOnly
If supplied, the integer will be included in a response but not in a request

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

### -Required
If supplied, the object will be treated as Required where supported.

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

### -UniqueItems
If supplied, specify that all items in the array must be unique

```yaml
Type: SwitchParameter
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriteOnly
If supplied, the integer will be included in a request but not in a response

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

### -XmlAttribute
Indicates whether the property should be serialized as an XML attribute, equivalent to the 'xml.attribute' attribute in OpenAPI.

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

### -XmlItemName
Specifically for properties treated as arrays, it defines the XML name for each item in the array.
This parameter aligns with the 'xml.name' attribute under 'items' in OpenAPI.

```yaml
Type: String
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XmlName
By default, XML elements get the same names that fields in the API declaration have.
This property change the XML name of the property
reflecting the 'xml.name' attribute in the OpenAPI specification.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XmlNamespace
Defines a specific XML namespace for the property, corresponding to the 'xml.namespace' attribute in OpenAPI.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XmlPrefix
Sets a prefix for the XML element name, aligning with the 'xml.prefix' attribute in OpenAPI.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XmlWrapped
Indicates whether array items should be wrapped in an XML element, similar to the 'xml.wrapped' attribute in OpenAPI.

```yaml
Type: SwitchParameter
Parameter Sets: Array
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

### System.Collections.Specialized.OrderedDictionary
## NOTES

## RELATED LINKS

[https://swagger.io/docs/specification/basic-structure/](https://swagger.io/docs/specification/basic-structure/)

[https://swagger.io/docs/specification/data-models/](https://swagger.io/docs/specification/data-models/)

