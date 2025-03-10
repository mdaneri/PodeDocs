---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Test-PodeOAJsonSchemaCompliance

## SYNOPSIS
Validate a parameter with a provided schema.

## SYNTAX

```
Test-PodeOAJsonSchemaCompliance [-Json] <Object> [-SchemaReference] <String> [[-DefinitionTag] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Validate the parameter of a method against it's own schema

## EXAMPLES

### EXAMPLE 1
```
$UserInfo = Test-PodeOAJsonSchemaCompliance -Json $UserInfo -SchemaReference 'UserIdSchema'}
```

## PARAMETERS

### -DefinitionTag
A string representing the unique tag for the API specification.
This tag helps distinguish between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Json
The object in Json format to validate

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

### -SchemaReference
The schema name to use to validate the property.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### result: true if the object is validate positively
### message: any validation issue
## NOTES

## RELATED LINKS
