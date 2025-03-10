---
external help file: Pode-help.xml
Module Name: Pode
online version: https://github.com/mrin9/RapiPdf
PodeType: OpenApi
schema: 2.0.0
---

# Enable-PodeOAViewer

## SYNOPSIS
Adds a route that enables a viewer to display OpenAPI docs, such as Swagger, ReDoc, RapiDoc, StopLight, Explorer, RapiPdf or Bookmarks.

## SYNTAX

### Doc (Default)
```
Enable-PodeOAViewer -Type <String> [-Path <String>] [-OpenApiUrl <String>] [-Middleware <Object[]>]
 [-Title <String>] [-DarkMode] [-EndpointName <String[]>] [-Authentication <String>] [-Role <String[]>]
 [-Group <String[]>] [-Scope <String[]>] [-DefinitionTag <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Bookmarks
```
Enable-PodeOAViewer [-Path <String>] [-OpenApiUrl <String>] [-Middleware <Object[]>] [-Title <String>]
 [-DarkMode] [-EndpointName <String[]>] [-Authentication <String>] [-Role <String[]>] [-Group <String[]>]
 [-Scope <String[]>] [-Bookmarks] [-NoAdvertise] [-DefinitionTag <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Editor
```
Enable-PodeOAViewer [-Path <String>] [-OpenApiUrl <String>] [-Middleware <Object[]>] [-Title <String>]
 [-DarkMode] [-EndpointName <String[]>] [-Authentication <String>] [-Role <String[]>] [-Group <String[]>]
 [-Scope <String[]>] [-Editor] [-DefinitionTag <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Adds a route that enables a viewer to display OpenAPI docs, such as Swagger, ReDoc, RapiDoc, StopLight, Explorer, RapiPdf  or Bookmarks.

## EXAMPLES

### EXAMPLE 1
```
Enable-PodeOAViewer -Type Swagger -DarkMode
```

### EXAMPLE 2
```
Enable-PodeOAViewer -Type ReDoc -Title 'Some Title' -OpenApi 'http://some-url/openapi'
```

### EXAMPLE 3
```
Enable-PodeOAViewer -Bookmarks
```

Adds a route that enables a viewer to display with links to any documentation tool associated with the OpenApi.

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

### -Bookmarks
If supplied, create a new documentation bookmarks page

```yaml
Type: SwitchParameter
Parameter Sets: Bookmarks
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DarkMode
If supplied, the page will be rendered using a dark theme (this is not supported for all viewers).

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

### -Editor
If supplied, enable the Swagger-Editor

```yaml
Type: SwitchParameter
Parameter Sets: Editor
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
The EndpointName of an Endpoint(s) to bind the static Route against.This parameter is normally not required.
The Endpoint is retrieved by the OpenAPI DefinitionTag

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

### -Middleware
Like normal Routes, an array of Middleware that will be applied.

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

### -NoAdvertise
If supplied, it is not going to state the documentation URL at the startup of the server

```yaml
Type: SwitchParameter
Parameter Sets: Bookmarks
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OpenApiUrl
The URL where the OpenAPI definition can be retrieved.
(Default is the OpenAPI path from Enable-PodeOpenApi)

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

### -Path
The route Path where the docs can be accessed.
(Default: "/$Type")

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
The title of the web page.
(Default is the OpenAPI title from Enable-PodeOpenApi)

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

### -Type
The Type of OpenAPI viewer to use.

```yaml
Type: String
Parameter Sets: Doc
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

[https://github.com/mrin9/RapiPdf](https://github.com/mrin9/RapiPdf)

[https://github.com/Authress-Engineering/openapi-explorer](https://github.com/Authress-Engineering/openapi-explorer)

[https://github.com/stoplightio/elements](https://github.com/stoplightio/elements)

[https://github.com/rapi-doc/RapiDoc](https://github.com/rapi-doc/RapiDoc)

[https://github.com/Redocly/redoc](https://github.com/Redocly/redoc)

[https://github.com/swagger-api/swagger-ui](https://github.com/swagger-api/swagger-ui)

