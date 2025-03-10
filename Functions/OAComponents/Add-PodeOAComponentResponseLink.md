---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OAComponents
schema: 2.0.0
---

# Add-PodeOAComponentResponseLink

## SYNOPSIS
Adds a reusable response link.

## SYNTAX

### OperationId (Default)
```
Add-PodeOAComponentResponseLink -Name <String> [-Description <String>] -OperationId <String>
 [-Parameters <Hashtable>] [-RequestBody <String>] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### OperationRef
```
Add-PodeOAComponentResponseLink -Name <String> [-Description <String>] -OperationRef <String>
 [-Parameters <Hashtable>] [-RequestBody <String>] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The Add-PodeOAComponentResponseLink function is designed to add a new reusable response link

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAComponentResponseLink   -Name 'address' -OperationId 'getUserByName' -Parameters @{'username' = '$request.path.username'}
Add-PodeOAResponse -StatusCode 200 -Content @{'application/json' = 'User'} -Links 'address'
This example demonstrates creating and adding a link named 'address' associated with the operation 'getUserByName' to an OrderedDictionary of links. The updated dictionary is then used in the 'Add-PodeOAResponse' function to define a response with a status code of 200.
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A brief description of the response link.
CommonMark syntax may be used for rich text representation.
For more information on CommonMark syntax, see \[CommonMark Specification\](https://spec.commonmark.org/).

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

### -Name
Mandatory.
A unique name for the response link.
Must be a valid string composed of alphanumeric characters, periods (.), hyphens (-), and underscores (_).

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

### -OperationId
The name of an existing, resolvable OpenAPI Specification (OAS) operation, as defined with a unique \`operationId\`.
This parameter is mandatory when using the 'OperationId' parameter set and is mutually exclusive of the \`OperationRef\` field.
It is used to specify the unique identifier of the operation the link is associated with.

```yaml
Type: String
Parameter Sets: OperationId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationRef
A relative or absolute URI reference to an OAS operation.
This parameter is mandatory when using the 'OperationRef' parameter set and is mutually exclusive of the \`OperationId\` field.
It MUST point to an Operation Object.
Relative \`operationRef\` values MAY be used to locate an existing Operation Object in the OpenAPI specification.

```yaml
Type: String
Parameter Sets: OperationRef
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameters
A map representing parameters to pass to an operation as specified with \`operationId\` or identified via \`operationRef\`.
The key is the parameter name to be used, whereas the value can be a constant or an expression to be evaluated and passed to the linked operation.
Parameter names can be qualified using the parameter location syntax \`\[{in}.\]{name}\` for operations that use the same parameter name in different locations (e.g., path.id).

```yaml
Type: Hashtable
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

### -RequestBody
A string representing the request body to use as a request body when calling the target.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
The function supports adding links either by specifying an 'OperationId' or an 'OperationRef', making it versatile for different OpenAPI specification needs.
It's important to match the parameters and response structures as per the OpenAPI specification to ensure the correct functionality of the API documentation.

## RELATED LINKS
