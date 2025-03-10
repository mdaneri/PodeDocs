---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Add-PodeOAServerEndpoint

## SYNOPSIS
Creates an OpenAPI Server Object.

## SYNTAX

```
Add-PodeOAServerEndpoint [-Url] <String> [[-Description] <String>] [[-Variables] <OrderedDictionary>]
 [[-DefinitionTag] <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates an OpenAPI Server Object.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAServerEndpoint -Url 'https://myserver.io/api' -Description 'My test server'
```

### EXAMPLE 2
```
Add-PodeOAServerEndpoint -Url '/api' -Description 'My local server'
```

### EXAMPLE 3
```
Add-PodeOAServerEndpoint -Url "https://{username}.gigantic-server.com:{port}/{basePath}" -Description "The production API server" `
    -Variable   @{
        username = @{
            default = 'demo'
            description = 'this value is assigned by the service provider, in this example gigantic-server.com'
        }
        port = @{
            enum = @('System.Object[]') # Assuming 'System.Object[]' is a placeholder for actual values
            default = 8443
        }
        basePath = @{
            default = 'v2'
        }
    }
}
```

## PARAMETERS

### -DefinitionTag
An Array of strings representing the unique tag for the API specification.
This tag helps distinguish between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
An optional string describing the host designated by the URL.
\[CommonMark syntax\](https://spec.commonmark.org/) MAY be used for rich text representation.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

### -Url
A URL to the target host. 
This URL supports Server Variables and MAY be relative, to indicate that the host location is relative to the location where the OpenAPI document is being served.
Variable substitutions will be made when a variable is named in \`{\`brackets\`}\`.

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

### -Variables
A map between a variable name and its value. 
The value is used for substitution in the server's URL template.

```yaml
Type: OrderedDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
