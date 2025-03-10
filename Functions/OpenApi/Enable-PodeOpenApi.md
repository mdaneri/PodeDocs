---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Enable-PodeOpenApi

## SYNOPSIS
Enables the OpenAPI default route in Pode.

## SYNTAX

### Deprecated
```
Enable-PodeOpenApi [-Path <String>] [-Title <String>] [-Version <String>] [-Description <String>]
 [-OpenApiVersion <String>] [-RouteFilter <String>] [-EndpointName <String[]>] [-Middleware <Object[]>]
 [-Authentication <String>] [-Role <String[]>] [-Group <String[]>] [-Scope <String[]>] [-RestrictRoutes]
 [-Mode <String>] [-MarkupLanguage <String>] [-EnableSchemaValidation] [-Depth <Int32>]
 [-DisableMinimalDefinitions] [-DefinitionTag <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### DefaultResponses
```
Enable-PodeOpenApi [-Path <String>] [-OpenApiVersion <String>] [-RouteFilter <String>]
 [-EndpointName <String[]>] [-Middleware <Object[]>] [-Authentication <String>] [-Role <String[]>]
 [-Group <String[]>] [-Scope <String[]>] [-RestrictRoutes] [-Mode <String>] [-MarkupLanguage <String>]
 [-EnableSchemaValidation] [-Depth <Int32>] [-DisableMinimalDefinitions] -DefaultResponses <Hashtable>
 [-DefinitionTag <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### NoDefaultResponses
```
Enable-PodeOpenApi [-Path <String>] [-OpenApiVersion <String>] [-RouteFilter <String>]
 [-EndpointName <String[]>] [-Middleware <Object[]>] [-Authentication <String>] [-Role <String[]>]
 [-Group <String[]>] [-Scope <String[]>] [-RestrictRoutes] [-Mode <String>] [-MarkupLanguage <String>]
 [-EnableSchemaValidation] [-Depth <Int32>] [-DisableMinimalDefinitions] [-NoDefaultResponses]
 [-DefinitionTag <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Enables the OpenAPI default route in Pode, as well as setting up details like Title and API Version.

## EXAMPLES

### EXAMPLE 1
```
Enable-PodeOpenApi -Title 'My API' -Version '1.0.0' -RouteFilter '/api/*'
```

### EXAMPLE 2
```
Enable-PodeOpenApi -Title 'My API' -Version '1.0.0' -RouteFilter '/api/*' -RestrictRoutes
```

### EXAMPLE 3
```
Enable-PodeOpenApi -Path '/docs/openapi'   -NoCompress -Mode 'Donwload' -DisableMinimalDefinitions
```

## PARAMETERS

### -Authentication
The name of an Authentication method which should be used as middleware on this Route.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Auth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultResponses
If supplied, it will replace the default OpenAPI response with the new provided.(Default: @{'200' = @{ description = 'OK' };'default' = @{ description = 'Internal server error' }} )

```yaml
Type: Hashtable
Parameter Sets: DefaultResponses
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionTag
A string representing the unique tag for the API specification.
This tag helps distinguish between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

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

### -Depth
Define the default  depth used by any JSON,YAML OpenAPI conversion (default 20)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A short description of the API.
(Deprecated -  Use Add-PodeOAInfo)
CommonMark syntax MAY be used for rich text representation.
https://spec.commonmark.org/

```yaml
Type: String
Parameter Sets: Deprecated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableMinimalDefinitions
If supplied the OpenApi decument will include only the route validated by Set-PodeOARouteInfo.
Any other not OpenApi route will be excluded.

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

### -EnableSchemaValidation
If supplied enable Test-PodeOAJsonSchemaCompliance  cmdlet that provide support for opeapi parameter schema validation

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

### -EndpointName
The EndpointName of an Endpoint(s) to bind the static Route against.

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

### -Group
One or more optional Groups that will be authorised to access this Route, when using Authentication with an Access method.

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

### -MarkupLanguage
Define the default markup language for the OpenApi spec ('Json', 'Json-Compress', 'Yaml')

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Json
Accept pipeline input: False
Accept wildcard characters: False
```

### -Middleware
Like normal Routes, an array of Middleware that will be applied to the route.

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

### -Mode
Define the way the OpenAPI definition file is accessed, the value can be View or Download.
(Default: View)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: View
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoDefaultResponses
If supplied, it will disable the default OpenAPI response with the new provided.

```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultResponses
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OpenApiVersion
Specify OpenApi Version (default: 3.0.3)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0.3
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
An optional custom route path to access the OpenAPI definition.
(Default: /openapi)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: /openapi
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

### -Role
One or more optional Roles that will be authorised to access this Route, when using Authentication with an Access method.

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

### -RouteFilter
An optional route filter for routes that should be included in the definition.
(Default: /*)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: /*
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
One or more optional Scopes that will be authorised to access this Route, when using Authentication with an Access method.

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

### -Title
The Title of the API.
(Deprecated -  Use Add-PodeOAInfo)

```yaml
Type: String
Parameter Sets: Deprecated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
The Version of the API. 
(Deprecated -  Use Add-PodeOAInfo)
The OpenAPI Specification is versioned using Semantic Versioning 2.0.0 (semver) and follows the semver specification.
https://semver.org/spec/v2.0.0.html

```yaml
Type: String
Parameter Sets: Deprecated
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
