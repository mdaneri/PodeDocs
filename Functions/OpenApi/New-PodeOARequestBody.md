---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# New-PodeOARequestBody

## SYNOPSIS
Creates a Request Body definition for routes.

## SYNTAX

### BuiltIn (Default)
```
New-PodeOARequestBody -Content <Hashtable> [-Description <String>] [-Required] [-Properties]
 [-Examples <OrderedDictionary>] [-Encoding <Hashtable[]>] [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Reference
```
New-PodeOARequestBody -Reference <String> [-Examples <OrderedDictionary>] [-Encoding <Hashtable[]>]
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a Request Body definition for routes from the supplied content-types and schemas.

## EXAMPLES

### EXAMPLE 1
```
New-PodeOARequestBody -Content @{ 'application/json' = (New-PodeOAIntProperty -Name 'userId' -Object) }
```

### EXAMPLE 2
```
New-PodeOARequestBody -Content @{ 'application/json' = 'UserIdSchema' }
```

### EXAMPLE 3
```
New-PodeOARequestBody -Reference 'UserIdBody'
```

### EXAMPLE 4
```
New-PodeOARequestBody -Content @{'multipart/form-data' =
                    New-PodeOAStringProperty -name 'id' -format 'uuid' |
                        New-PodeOAObjectProperty -name 'address' -NoProperties |
                        New-PodeOAObjectProperty -name 'historyMetadata' -Description 'metadata in XML format' -NoProperties |
                        New-PodeOAStringProperty -name 'profileImage' -Format Binary |
                        New-PodeOAObjectProperty
                    } -Encoding (
                        New-PodeOAEncodingObject -Name 'historyMetadata' -ContentType 'application/xml; charset=utf-8' |
                            New-PodeOAEncodingObject -Name 'profileImage' -ContentType 'image/png, image/jpeg' -Headers (
                                New-PodeOAIntProperty -name 'X-Rate-Limit-Limit' -Description 'The number of allowed requests in the current period' -Default 3 -Enum @(1,2,3)
                            )
                        )
```

## PARAMETERS

### -Content
The content of the request body.
The key is a media type or media type range and the value describes it.
For requests that match multiple keys, only the most specific key is applicable.
e.g.
text/plain overrides text/*
Alias: ContentSchemas

```yaml
Type: Hashtable
Parameter Sets: BuiltIn
Aliases: ContentSchemas

Required: True
Position: Named
Default value: None
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
A brief description of the request body.
This could contain examples of use.
CommonMark syntax MAY be used for rich text representation.

```yaml
Type: String
Parameter Sets: BuiltIn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Encoding
This parameter give you control over the serialization of parts of multipart request bodies.
This attribute is only applicable to multipart and application/x-www-form-urlencoded request bodies.
Use New-PodeOAEncodingObject to define the encode

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Examples
Supplied an Example of the media type. 
The example object SHOULD be in the correct format as specified by the media type.
The \`example\` field is mutually exclusive of the \`examples\` field.
Furthermore, if referencing a \`schema\` which contains an example, the \`example\` value SHALL _override_ the example provided by the schema.

```yaml
Type: OrderedDictionary
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

### -Properties
Use to force the use of the properties keyword under a schema.
Commonly used to specify a multipart/form-data multi file

```yaml
Type: SwitchParameter
Parameter Sets: BuiltIn
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reference
A reference name from an existing component request body.
Alias: Reference

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

### -Required
Determines if the request body is required in the request.
Defaults to false.

```yaml
Type: SwitchParameter
Parameter Sets: BuiltIn
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable
### System.Collections.Specialized.OrderedDictionary
## NOTES

## RELATED LINKS
