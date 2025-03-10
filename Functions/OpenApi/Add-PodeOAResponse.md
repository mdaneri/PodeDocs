---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Add-PodeOAResponse

## SYNOPSIS
Adds a response definition to the supplied route.

## SYNTAX

### Schema (Default)
```
Add-PodeOAResponse [-Route] <Hashtable[]> -StatusCode <String> [-Content <Hashtable>] [-Headers <Object>]
 [-Description <String>] [-Links <OrderedDictionary>] [-PassThru] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Reference
```
Add-PodeOAResponse [-Route] <Hashtable[]> -StatusCode <String> [-Headers <Object>] -Reference <String>
 [-PassThru] [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### SchemaDefault
```
Add-PodeOAResponse [-Route] <Hashtable[]> [-Content <Hashtable>] [-Headers <Object>] [-Description <String>]
 [-Default] [-Links <OrderedDictionary>] [-PassThru] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ReferenceDefault
```
Add-PodeOAResponse [-Route] <Hashtable[]> [-Headers <Object>] [-Reference <String>] [-Default] [-PassThru]
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a response definition to the supplied route.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeRoute -PassThru | Add-PodeOAResponse -StatusCode 200 -Content @{ 'application/json' = (New-PodeOAIntProperty -Name 'userId' -Object) }
```

### EXAMPLE 2
```
Add-PodeRoute -PassThru | Add-PodeOAResponse -StatusCode 200 -Content @{ 'application/json' = 'UserIdSchema' }
```

### EXAMPLE 3
```
Add-PodeRoute -PassThru | Add-PodeOAResponse -StatusCode 200 -Reference 'OKResponse'
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

Required: False
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

### -Route
The route to add the response definition, usually from -PassThru on Add-PodeRoute.

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: True
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

### System.Collections.Hashtable[]
## NOTES

## RELATED LINKS
