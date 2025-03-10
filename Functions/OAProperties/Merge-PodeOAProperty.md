---
external help file: Pode-help.xml
Module Name: Pode
online version: https://swagger.io/docs/specification/basic-structure/
PodeType: OAProperties
schema: 2.0.0
---

# Merge-PodeOAProperty

## SYNOPSIS
Creates a new OpenAPI object combining schemas and properties.

## SYNTAX

### Inbuilt (Default)
```
Merge-PodeOAProperty [[-ParamsList] <Hashtable[]>] -Type <String> [-ObjectDefinitions <Object[]>]
 [-DiscriminatorProperty <String>] [-DiscriminatorMapping <Hashtable>] [-NoObjectDefinitionsFromPipeline]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Name
```
Merge-PodeOAProperty [[-ParamsList] <Hashtable[]>] -Type <String> [-ObjectDefinitions <Object[]>]
 [-DiscriminatorProperty <String>] [-DiscriminatorMapping <Hashtable>] [-NoObjectDefinitionsFromPipeline]
 -Name <String> [-Required] [-Description <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new OpenAPI object combining schemas and properties.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAComponentSchema -Name 'Pets' -Component (Merge-PodeOAProperty -Type OneOf -ObjectDefinitions @('Cat', 'Dog') -Discriminator "petType")
```

### EXAMPLE 2
```
Add-PodeOAComponentSchema -Name 'Cat' -Component (
    Merge-PodeOAProperty -Type AllOf -ObjectDefinitions @(
        'Pet',
        (New-PodeOAObjectProperty -Properties @(
            (New-PodeOAStringProperty -Name 'huntingSkill' -Description 'The measured skill for hunting' -Enum @('clueless', 'lazy', 'adventurous', 'aggressive'))
        ))
    )
)
```

## PARAMETERS

### -Description
Provides a description for the OpenAPI object.

```yaml
Type: String
Parameter Sets: Name
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiscriminatorMapping
If supplied, defines a mapping between the values of the discriminator property and the corresponding subtype schemas.
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

### -Name
Specifies the name of the OpenAPI object.

```yaml
Type: String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoObjectDefinitionsFromPipeline
Prevents object definitions from being used in the computation but still passes them through the pipeline.

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

### -ObjectDefinitions
An array of object definitions that are used for independent validation but together compose a single object.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParamsList
Used to pipeline an object definition

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

### -Required
Indicates if the object is required.

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Define the type of validation between the objects
oneOf - validates the value against exactly one of the subschemas
allOf - validates the value against all the subschemas
anyOf - validates the value against any (one or more) of the subschemas

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Specialized.OrderedDictionary
## NOTES

## RELATED LINKS

[https://swagger.io/docs/specification/basic-structure/](https://swagger.io/docs/specification/basic-structure/)

[https://swagger.io/docs/specification/data-models/](https://swagger.io/docs/specification/data-models/)

