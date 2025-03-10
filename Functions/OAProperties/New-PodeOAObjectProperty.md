---
external help file: Pode-help.xml
Module Name: Pode
online version: https://swagger.io/docs/specification/basic-structure/
PodeType: OAProperties
schema: 2.0.0
---

# New-PodeOAObjectProperty

## SYNOPSIS
Creates a new OpenAPI object property from other properties.

## SYNTAX

### Inbuilt (Default)
```
New-PodeOAObjectProperty [[-ParamsList] <Hashtable[]>] [-Name <String>] [-Properties <Hashtable[]>]
 [-Description <String>] [-ExternalDoc <String>] [-Example <Object>] [-Deprecated] [-Required] [-Nullable]
 [-ReadOnly] [-WriteOnly] [-NoProperties] [-MinProperties <Int32>] [-MaxProperties <Int32>]
 [-NoAdditionalProperties] [-AdditionalProperties <Hashtable>] [-XmlName <String>] [-XmlNamespace <String>]
 [-XmlPrefix <String>] [-XmlAttribute] [-DiscriminatorProperty <String>] [-DiscriminatorMapping <Hashtable>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Array
```
New-PodeOAObjectProperty [[-ParamsList] <Hashtable[]>] [-Name <String>] [-Properties <Hashtable[]>]
 [-Description <String>] [-ExternalDoc <String>] [-Example <Object>] [-Deprecated] [-Required] [-Nullable]
 [-ReadOnly] [-WriteOnly] [-NoProperties] [-MinProperties <Int32>] [-MaxProperties <Int32>]
 [-NoAdditionalProperties] [-AdditionalProperties <Hashtable>] [-XmlName <String>] [-XmlNamespace <String>]
 [-XmlPrefix <String>] [-XmlAttribute] [-XmlItemName <String>] [-XmlWrapped] [-Array] [-UniqueItems]
 [-MinItems <Int32>] [-MaxItems <Int32>] [-DiscriminatorProperty <String>] [-DiscriminatorMapping <Hashtable>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new OpenAPI object property from other properties, for Schemas or Parameters.

## EXAMPLES

### EXAMPLE 1
```
')
```

### EXAMPLE 2
```
New-PodeOABoolProperty -Name 'enabled' -Required|
    New-PodeOAObjectProperty  -Name 'extraProperties'  -AdditionalProperties [ordered]@{
        "property1" = [ordered]@{ "type" = "string"; "description" = "Description for property1" };
        "property2" = [ordered]@{ "type" = "integer"; "format" = "int32" }
}
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

### -DiscriminatorMapping
If supplied, define a mapping between the values of the discriminator property and the corresponding subtype schemas.
This parameter accepts a HashTable where each key-value pair maps a discriminator value to a specific subtype schema name.
It's used in conjunction with the -DiscriminatorProperty to provide complete discrimination logic in polymorphic scenarios.

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

### -DiscriminatorProperty
If supplied, specifies the name of the property used to distinguish between different subtypes in a polymorphic schema in OpenAPI.
This string value represents the property in the payload that indicates which specific subtype schema should be applied.
It's essential in scenarios where an API endpoint handles data that conforms to one of several derived schemas from a common base schema.

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

### -MaxProperties
If supplied, will restrict the maximum number of properties allowed in an object.

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

### -MinProperties
If supplied, will restrict the minimun number of properties allowed in an object.

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

### -NoProperties
If supplied, no properties are allowed in the object.
If no properties are assigned to the object and the NoProperties parameter is not set the object accept any property

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
If supplied, the object will be treated as Nullable.

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

### -Properties
An array of other int/string/etc properties wrap up as an object.

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadOnly
If supplied, the object will be included in a response but not in a request

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
If supplied, the object will be included in a request but not in a response

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

## NOTES

## RELATED LINKS

[https://swagger.io/docs/specification/basic-structure/](https://swagger.io/docs/specification/basic-structure/)

[https://swagger.io/docs/specification/data-models/](https://swagger.io/docs/specification/data-models/)

