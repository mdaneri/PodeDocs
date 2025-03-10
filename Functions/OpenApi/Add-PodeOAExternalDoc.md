---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Add-PodeOAExternalDoc

## SYNOPSIS
Add an external docs reference to the OpenApi document.

## SYNTAX

### Pipe (Default)
```
Add-PodeOAExternalDoc [[-ExternalDoc] <OrderedDictionary>] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### NewRef
```
Add-PodeOAExternalDoc -Url <Object> [-Description <String>] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Add an external docs reference to the OpenApi document.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAExternalDoc  -Name 'SwaggerDocs' -Description 'Find out more about Swagger' -Url 'http://swagger.io'
```

### EXAMPLE 2
```
$ExtDoc = New-PodeOAExternalDoc  -Name 'SwaggerDocs' -Description 'Find out more about Swagger' -Url 'http://swagger.io'
$ExtDoc|Add-PodeOAExternalDoc
```

## PARAMETERS

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

### -Description
A Description of the external documentation.

```yaml
Type: String
Parameter Sets: NewRef
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalDoc
An externalDoc object

```yaml
Type: OrderedDictionary
Parameter Sets: Pipe
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

### -Url
The link to the external documentation

```yaml
Type: Object
Parameter Sets: NewRef
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
