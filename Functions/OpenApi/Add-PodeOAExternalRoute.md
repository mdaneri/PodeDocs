---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Add-PodeOAExternalRoute

## SYNOPSIS
Sets metadate for the supplied route.

## SYNTAX

### Pipeline (Default)
```
Add-PodeOAExternalRoute [-Route] <Hashtable[]> -Servers <Hashtable[]> [-PassThru]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### BuiltIn
```
Add-PodeOAExternalRoute -Path <String> -Servers <Hashtable[]> -Method <String> [-PassThru]
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Sets metadate for the supplied route, such as Summary and Tags.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAExternalRoute -PassThru -Method Get -Path '/peta/:id' -Servers (
    New-PodeOAServerEndpoint -Url 'http://ext.server.com/api/v12' -Description 'ext test server' |
    New-PodeOAServerEndpoint -Url 'http://ext13.server.com/api/v12' -Description 'ext test server 13'
    ) |
        Set-PodeOARouteInfo -Summary 'Find pets by ID' -Description 'Returns pets based on ID'  -OperationId 'getPetsById' -PassThru |
        Set-PodeOARequest -PassThru -Parameters @(
        (New-PodeOAStringProperty -Name 'id' -Description 'ID of pet to use' -array | ConvertTo-PodeOAParameter -In Path -Style Simple -Required )) |
        Add-PodeOAResponse -StatusCode 200 -Description 'pet response'   -Content (@{ '*/*' = New-PodeOASchemaProperty   -ComponentSchema 'Pet' -array }) -PassThru |
        Add-PodeOAResponse -Default  -Description 'error payload' -Content (@{'text/html' = 'ErrorModel' }) -PassThru
```

### EXAMPLE 2
```
Add-PodeRoute -PassThru -Method Get -Path '/peta/:id'  -ScriptBlock {
        Write-PodeJsonResponse -Value 'done' -StatusCode 200
    } | Add-PodeOAExternalRoute -PassThru   -Servers (
    New-PodeOAServerEndpoint -Url 'http://ext.server.com/api/v12' -Description 'ext test server' |
    New-PodeOAServerEndpoint -Url 'http://ext13.server.com/api/v12' -Description 'ext test server 13'
    ) |
    Set-PodeOARouteInfo -Summary 'Find pets by ID' -Description 'Returns pets based on ID'  -OperationId 'getPetsById' -PassThru |
    Set-PodeOARequest -PassThru -Parameters @(
    (New-PodeOAStringProperty -Name 'id' -Description 'ID of pet to use' -array | ConvertTo-PodeOAParameter -In Path -Style Simple -Required )) |
    Add-PodeOAResponse -StatusCode 200 -Description 'pet response'   -Content (@{ '*/*' = New-PodeOASchemaProperty   -ComponentSchema 'Pet' -array }) -PassThru |
    Add-PodeOAResponse -Default  -Description 'error payload' -Content (@{'text/html' = 'ErrorModel' }) -PassThru
```

## PARAMETERS

### -DefinitionTag
An Array of strings representing the unique tag for the API specification.
This tag helps distinguish between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

```yaml
Type: String[]
Parameter Sets: BuiltIn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
The HTTP Method of this Route, multiple can be supplied.

```yaml
Type: String
Parameter Sets: BuiltIn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
If supplied, the route passed in will be returned for further chaining.

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

### -Path
The URI path for the Route.

```yaml
Type: String
Parameter Sets: BuiltIn
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

### -Route
The route to update info, usually from -PassThru on Add-PodeRoute.

```yaml
Type: Hashtable[]
Parameter Sets: Pipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Servers
A list of external endpoint.
created with New-PodeOAServerEndpoint

```yaml
Type: Hashtable[]
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

### System.Collections.Hashtable[]
### System.Collections.Hashtable
## NOTES

## RELATED LINKS
