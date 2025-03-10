---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# New-PodeOAResponse

## SYNOPSIS
Adds a response definition to the Callback.

## SYNTAX

### Schema (Default)
```
New-PodeOAResponse [[-ResponseList] <Hashtable>] -StatusCode <String> [-Content <Hashtable>]
 [-Headers <Object>] -Description <String> [-Links <OrderedDictionary>] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Reference
```
New-PodeOAResponse [[-ResponseList] <Hashtable>] -StatusCode <String> [-Headers <Object>] -Reference <String>
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### SchemaDefault
```
New-PodeOAResponse [[-ResponseList] <Hashtable>] [-Content <Hashtable>] [-Headers <Object>]
 -Description <String> [-Default] [-Links <OrderedDictionary>] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ReferenceDefault
```
New-PodeOAResponse [[-ResponseList] <Hashtable>] [-Headers <Object>] [-Reference <String>] [-Default]
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a response definition to the Callback.

## EXAMPLES

### EXAMPLE 1
```
New-PodeOAResponse -StatusCode 200 -Content (  New-PodeOAContentMediaType -ContentType 'application/json' -Content(New-PodeOAIntProperty -Name 'userId' -Object) )
```

### EXAMPLE 2
```
New-PodeOAResponse -StatusCode 200 -Content @{ 'application/json' = 'UserIdSchema' }
```

### EXAMPLE 3
```
New-PodeOAResponse -StatusCode 200 -Reference 'OKResponse'
```

### EXAMPLE 4
```
Add-PodeOACallBack -Title 'test' -Path '$request.body#/id' -Method Post  -RequestBody (
        New-PodeOARequestBody -Content (New-PodeOAContentMediaType -ContentType '*/*' -Content (New-PodeOAStringProperty -Name 'id'))
    ) `
    -Response (
        New-PodeOAResponse -StatusCode 200 -Description 'Successful operation' -Content (New-PodeOAContentMediaType -ContentType 'application/json','application/xml' -Content 'Pet'  -Array) |
            New-PodeOAResponse -StatusCode 400 -Description 'Invalid ID supplied' |
                New-PodeOAResponse -StatusCode 404 -Description 'Pet not found' |
            New-PodeOAResponse -Default   -Description 'Something is wrong'
            )
```

## PARAMETERS

### -Content
The content-types and schema the response returns (the schema is created using the Property functions).
Alias: ContentSchemas

```yaml
Type: Hashtable
Parameter Sets: Schema, SchemaDefault
Aliases: ContentSchemas

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Default
If supplied, the response will be used as a default response - this overrides the StatusCode supplied.

```yaml
Type: SwitchParameter
Parameter Sets: SchemaDefault, ReferenceDefault
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

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
A Description of the response.
(Default: the HTTP StatusCode description)

```yaml
Type: String
Parameter Sets: Schema, SchemaDefault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Headers
The header name and schema the response returns (the schema is created using Add-PodeOAComponentHeader cmd-let).
Alias: HeaderSchemas

```yaml
Type: Object
Parameter Sets: (All)
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
Parameter Sets: Schema, SchemaDefault
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

```yaml
Type: String
Parameter Sets: ReferenceDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResponseList
Hidden parameter used to pipe multiple CallBacksResponses

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
The HTTP StatusCode for the response.To define a range of response codes, this field MAY contain the uppercase wildcard character \`X\`.
For example, \`2XX\` represents all response codes between \`\[200-299\]\`.
Only the following range definitions are allowed: \`1XX\`, \`2XX\`, \`3XX\`, \`4XX\`, and \`5XX\`.
If a response is defined using an explicit code, the explicit code definition takes precedence over the range definition for that code.

```yaml
Type: String
Parameter Sets: Schema, Reference
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

### System.Collections.Hashtable
## NOTES

## RELATED LINKS
