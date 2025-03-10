---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Get-PodeOADefinition

## SYNOPSIS
Gets the OpenAPI definition.

## SYNTAX

```
Get-PodeOADefinition [[-Format] <String>] [[-Title] <String>] [[-Version] <String>] [[-Description] <String>]
 [[-RouteFilter] <String>] [-RestrictRoutes] [[-DefinitionTag] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Gets the OpenAPI definition for custom use in routes, or other functions.

## EXAMPLES

### EXAMPLE 1
```
$defInJson = Get-PodeOADefinition -Json
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
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A Description of the API.
(Default: the description supplied into Enable-PodeOpenApi)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Format
Return the definition  in a specific format 'Json', 'Json-Compress', 'Yaml', 'HashTable'

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: HashTable
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

### -RestrictRoutes
If supplied, only routes that are available on the Requests URI will be used to generate the OpenAPI definition.

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

### -RouteFilter
An optional route filter for routes that should be included in the definition.
(Default: /*)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: /*
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
The Title of the API.
(Default: the title supplied in Enable-PodeOpenApi)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
The Version of the API.
(Default: the version supplied in Enable-PodeOpenApi)

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
