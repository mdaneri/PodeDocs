---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# ConvertTo-PodeOAParameter

## SYNOPSIS
Converts an OpenAPI property into a Request Parameter.

## SYNTAX

### Reference (Default)
```
ConvertTo-PodeOAParameter -Reference <String> [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### ContentProperties
```
ConvertTo-PodeOAParameter -In <String> [-Property] <Hashtable> [-Name <String>] -ContentType <String>
 [-Description <String>] [-Required] [-Example <Object>] [-Examples <OrderedDictionary>] [-Deprecated]
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ContentSchema
```
ConvertTo-PodeOAParameter -In <String> [-Name <String>] -Schema <String> -ContentType <String>
 [-Description <String>] [-Required] [-AllowEmptyValue] [-Example <Object>] [-Examples <OrderedDictionary>]
 [-Deprecated] [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Properties
```
ConvertTo-PodeOAParameter -In <String> [-Property] <Hashtable> [-Name <String>] [-Description <String>]
 [-Explode] [-Required] [-AllowEmptyValue] [-AllowReserved] [-Example <Object>] [-Examples <OrderedDictionary>]
 [-Style <String>] [-Deprecated] [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Schema
```
ConvertTo-PodeOAParameter -In <String> [-Name <String>] -Schema <String> [-Description <String>] [-Explode]
 [-Required] [-AllowEmptyValue] [-AllowReserved] [-Example <Object>] [-Examples <OrderedDictionary>]
 [-Style <String>] [-Deprecated] [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Converts an OpenAPI property (such as from New-PodeOAIntProperty) into a Request Parameter.

## EXAMPLES

### EXAMPLE 1
```
New-PodeOAIntProperty -Name 'userId' | ConvertTo-PodeOAParameter -In Query
```

### EXAMPLE 2
```
ConvertTo-PodeOAParameter -Reference 'UserIdParam'
```

### EXAMPLE 3
```
ConvertTo-PodeOAParameter  -In Header -ContentSchemas @{ 'application/json' = 'UserIdSchema' }
```

## PARAMETERS

### -AllowEmptyValue
If supplied, allow the parameter to be empty

```yaml
Type: SwitchParameter
Parameter Sets: ContentSchema, Properties, Schema
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowReserved
If supplied, determines whether the parameter value SHOULD allow reserved characters, as defined by RFC3986 :/?#\[\]@!$&'()*+,;= to be included without percent-encoding.
This property only applies to parameters with an in value of query.
The default value is false.

```yaml
Type: SwitchParameter
Parameter Sets: Properties, Schema
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentType
The content-types to be use with  component schema

```yaml
Type: String
Parameter Sets: ContentProperties, ContentSchema
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionTag
An Array of strings representing the unique tag for the API specification.
This tag helps distinguish between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Deprecated
If supplied, specifies that a parameter is deprecated and SHOULD be transitioned out of usage.
Default value is false.

```yaml
Type: SwitchParameter
Parameter Sets: ContentProperties, ContentSchema, Properties, Schema
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
Parameter Sets: ContentProperties, ContentSchema, Properties, Schema
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Example
Example of the parameter's potential value.
The example SHOULD match the specified schema and encoding properties if present.
The Example parameter is mutually exclusive of the Examples parameter.
Furthermore, if referencing a Schema  that contains an example, the Example value SHALL _override_ the example provided by the schema.
To represent examples of media types that cannot naturally be represented in JSON or YAML, a string value can contain the example with escaping where necessary.

```yaml
Type: Object
Parameter Sets: ContentProperties, ContentSchema, Properties, Schema
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Examples
Examples of the parameter's potential value.
Each example SHOULD contain a value in the correct format as specified in the parameter encoding.
The Examples parameter is mutually exclusive of the Example parameter.
Furthermore, if referencing a Schema that contains an example, the Examples value SHALL _override_ the example provided by the schema.

```yaml
Type: OrderedDictionary
Parameter Sets: ContentProperties, ContentSchema, Properties, Schema
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Explode
If supplied, controls how arrays are serialized in query parameters

```yaml
Type: SwitchParameter
Parameter Sets: Properties, Schema
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -In
Where in the Request can the parameter be found?

```yaml
Type: String
Parameter Sets: ContentProperties, ContentSchema, Properties, Schema
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Assign a name to the parameter

```yaml
Type: String
Parameter Sets: ContentProperties, ContentSchema, Properties, Schema
Aliases:

Required: False
Position: Named
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

### -Property
The Property that need converting (such as from New-PodeOAIntProperty).

```yaml
Type: Hashtable
Parameter Sets: ContentProperties, Properties
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Reference
The name of an existing component parameter to be reused.
Alias: ComponentParameter

```yaml
Type: String
Parameter Sets: Reference
Aliases: ComponentParameter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Required
If supplied, the object will be treated as Required where supported.(Applicable only to ContentSchema)

```yaml
Type: SwitchParameter
Parameter Sets: ContentProperties, ContentSchema, Properties, Schema
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schema
The component schema to use.

```yaml
Type: String
Parameter Sets: ContentSchema, Schema
Aliases: ComponentSchema

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Style
If supplied, defines how multiple values are delimited.
Possible styles depend on the parameter location: path, query, header or cookie.

```yaml
Type: String
Parameter Sets: Properties, Schema
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
