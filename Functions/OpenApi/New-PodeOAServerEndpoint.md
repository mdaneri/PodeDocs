---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# New-PodeOAServerEndpoint

## SYNOPSIS
Creates an OpenAPI Server Object.

## SYNTAX

```
New-PodeOAServerEndpoint [[-ServerEndpointList] <Hashtable[]>] -Url <String> [-Description <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates an OpenAPI Server Object to use with Add-PodeOAExternalRoute

## EXAMPLES

### EXAMPLE 1
```
New-PodeOAServerEndpoint -Url 'https://myserver.io/api' -Description 'My test server'
```

### EXAMPLE 2
```
New-PodeOAServerEndpoint -Url '/api' -Description 'My local server'
```

## PARAMETERS

### -Description
An optional string describing the host designated by the URL.
\[CommonMark syntax\](https://spec.commonmark.org/) MAY be used for rich text representation.

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

### -ServerEndpointList
Used for piping

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

### -Url
A URL to the target host. 
This URL supports Server Variables and MAY be relative, to indicate that the host location is relative to the location where the OpenAPI document is being served.
Variable substitutions will be made when a variable is named in \`{\`brackets\`}\`.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
