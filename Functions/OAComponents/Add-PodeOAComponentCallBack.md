---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OAComponents
schema: 2.0.0
---

# Add-PodeOAComponentCallBack

## SYNOPSIS
Adds OpenAPI reusable callback configurations.

## SYNTAX

```
Add-PodeOAComponentCallBack [-Name] <String> [-Path] <String> [-Method] <String> [[-Parameters] <Hashtable[]>]
 [[-RequestBody] <Hashtable>] [[-Responses] <Hashtable>] [[-DefinitionTag] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The Add-PodeOACallBack function is used for defining OpenAPI callback configurations for routes in a Pode server.
It enables setting up API specifications including detailed parameters, request body schemas, and response structures for various HTTP methods.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAComponentCallBack -Title 'test' -Path '{$request.body#/id}' -Method Post `
    -RequestBody (New-PodeOARequestBody -Content @{'*/*' = (New-PodeOAStringProperty -Name 'id')}) `
    -Response (
        New-PodeOAResponse -StatusCode 200 -Description 'Successful operation'  -Content (New-PodeOAContentMediaType -ContentType 'application/json','application/xml' -Content 'Pet'  -Array)
        New-PodeOAResponse -StatusCode 400 -Description 'Invalid ID supplied' |
        New-PodeOAResponse -StatusCode 404 -Description 'Pet not found' |
        New-PodeOAResponse -Default -Description 'Something is wrong'
    )
Add-PodeOACallBack -Reference 'test'
    This example demonstrates adding a POST callback to handle a request body and define various responses based on different status codes.
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
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
Defines the HTTP method for the callback (e.g., GET, POST, PUT).
Supports standard HTTP methods and a wildcard (*) for all methods.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Alias for 'Name'.
A unique identifier for the callback.
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

### -Parameters
The Parameter definitions the request uses (from ConvertTo-PodeOAParameter).

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the callback path, usually a relative URL.
The key that identifies the Path Item Object is a runtime expression evaluated in the context of a runtime HTTP request/response to identify the URL for the callback request.
A simple example is \`$request.body#/url\`.
The runtime expression allows complete access to the HTTP message, including any part of a body that a JSON Pointer (RFC6901) can reference.
More information on JSON Pointer can be found at \[RFC6901\](https://datatracker.ietf.org/doc/html/rfc6901).

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

### -RequestBody
Defines the schema of the request body.
Can be set using New-PodeOARequestBody.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Responses
Defines the possible responses for the callback.
Can be set using New-PodeOAResponse.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
Ensure that the provided parameters match the expected schema and formats of Pode and OpenAPI specifications.
The function is useful for dynamically configuring and documenting API callbacks in a Pode server environment.

## RELATED LINKS
