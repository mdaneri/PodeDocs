---
external help file: Pode-help.xml
Module Name: Pode
online version: https://swagger.io/docs/specification/paths-and-operations/
PodeType: OAComponents
schema: 2.0.0
---

# Add-PodeOAComponentPathItem

## SYNOPSIS
Sets metadate for the supplied route.

## SYNTAX

```
Add-PodeOAComponentPathItem [-Name] <String> [-Method] <String> [-PassThru] [[-DefinitionTag] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
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
Add-PodeOAComponentPathItem -PassThru -Method Get -Path '/peta/:id'  -ScriptBlock {
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
This tag helps in distinguishing between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
The HTTP Method of this Route, multiple can be supplied.

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

### -Name
Alias for 'Name'.
A unique identifier for the route.
It must be a valid string of alphanumeric characters, periods (.), hyphens (-), and underscores (_).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[https://swagger.io/docs/specification/paths-and-operations/](https://swagger.io/docs/specification/paths-and-operations/)

