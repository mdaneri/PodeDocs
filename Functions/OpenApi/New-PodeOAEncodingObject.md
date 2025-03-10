---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# New-PodeOAEncodingObject

## SYNOPSIS
Adds a single encoding definition applied to a single schema property.

## SYNTAX

```
New-PodeOAEncodingObject [[-EncodingList] <Hashtable[]>] -Title <String> [-ContentType <String>]
 [-Headers <Hashtable[]>] [-Style <String>] [-Explode] [-AllowReserved] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
A single encoding definition applied to a single schema property.

## EXAMPLES

### EXAMPLE 1
```
New-PodeOAEncodingObject -Name 'profileImage' -ContentType 'image/png, image/jpeg' -Headers (
                                New-PodeOAIntProperty -name 'X-Rate-Limit-Limit' -Description 'The number of allowed requests in the current period' -Default 3 -Enum @(1,2,3) -Maximum 3
                            )
```

## PARAMETERS

### -AllowReserved
Determines whether the parameter value SHOULD allow reserved characters, as defined by \[RFC3986\](https://tools.ietf.org/html/rfc3986#section-2.2) \`:/?#\[\]@!$&'()*+,;=\` to be included without percent-encoding.
This property SHALL be ignored if the request body media type is not \`application/x-www-form-urlencoded\`.

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

### -ContentType
Content-Type for encoding a specific property.
Default value depends on the property type: for \`string\` with \`format\` being \`binary\` - \`application/octet-stream\`;
for other primitive types - \`text/plain\`; for \`object\` - \`application/json\`; for \`array\` - the default is defined based on the inner type.
The value can be a specific media type (e.g.
\`application/json\`), a wildcard media type (e.g.
\`image/*\`), or a comma-separated list of the two types.

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

### -EncodingList
Used by pipe

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Explode
When enabled, property values of type \`array\` or \`object\` generate separate parameters for each value of the array, or key-value-pair of the map. 
For other types of properties this property has no effect.
When \[\`style\`\](#encodingStyle) is \`form\`, the \`Explode\` is set to \`true\`.
This property SHALL be ignored if the request body media type is not \`application/x-www-form-urlencoded\`.

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

### -Headers
A map allowing additional information to be provided as headers, for example \`Content-Disposition\`.
\`Content-Type\` is described separately and SHALL be ignored in this section.
This property SHALL be ignored if the request body media type is not a \`multipart\`.

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

### -Style
Describes how a specific property value will be serialized depending on its type. 
See \[Parameter Object\](#parameterObject) for details on the \[\`style\`\](#parameterStyle) property.
The behavior follows the same values as \`query\` parameters, including default values.
This property SHALL be ignored if the request body media type is not \`application/x-www-form-urlencoded\`.

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

### -Title
The Name of the associated encoded property .

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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
