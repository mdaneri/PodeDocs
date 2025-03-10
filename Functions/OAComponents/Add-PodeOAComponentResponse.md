---
external help file: Pode-help.xml
Module Name: Pode
online version: https://swagger.io/docs/specification/basic-structure/
PodeType: OAComponents
schema: 2.0.0
---

# Add-PodeOAComponentResponse

## SYNOPSIS
Adds a reusable component for responses.

## SYNTAX

### Schema (Default)
```
Add-PodeOAComponentResponse -Name <String> [-Content <Hashtable>] [-Headers <Object>] [-Description <String>]
 [-Links <OrderedDictionary>] [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Reference
```
Add-PodeOAComponentResponse -Name <String> -Reference <String> [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a reusable component for responses.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAComponentResponse -Name 'OKResponse' -Content @{ 'application/json' = (New-PodeOAIntProperty -Name 'userId' -Object) }
```

### EXAMPLE 2
```
Add-PodeOAComponentResponse -Name 'ErrorResponse' -Content  @{ 'application/json' = 'ErrorSchema' }
```

## PARAMETERS

### -Content
The content-types and schema the response returns (the schema is created using the Property functions).

```yaml
Type: Hashtable
Parameter Sets: Schema
Aliases: ContentSchemas

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionTag
An Array of strings representing the unique tag for the API specification.
This tag helps in distinguishing between different versions or types of API specifications within the application.
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

### -Description
The Description of the response.

```yaml
Type: String
Parameter Sets: Schema
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Headers
The header name and schema the response returns (the schema is created using the Add-PodeOAComponentHeader cmdlet).

```yaml
Type: Object
Parameter Sets: Schema
Aliases: HeaderSchemas

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Links
A Response link definition

```yaml
Type: OrderedDictionary
Parameter Sets: Schema
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The reference Name of the response.

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

### -Reference
A Reference Name of an existing component response to use.

```yaml
Type: String
Parameter Sets: Reference
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

## NOTES

## RELATED LINKS

[https://swagger.io/docs/specification/basic-structure/](https://swagger.io/docs/specification/basic-structure/)

[https://swagger.io/docs/specification/data-models/](https://swagger.io/docs/specification/data-models/)

[https://swagger.io/docs/specification/serialization/](https://swagger.io/docs/specification/serialization/)

