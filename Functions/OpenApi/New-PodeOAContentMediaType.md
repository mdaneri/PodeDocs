---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# New-PodeOAContentMediaType

## SYNOPSIS
Creates media content type definitions for OpenAPI specifications.

## SYNTAX

### inbuilt (Default)
```
New-PodeOAContentMediaType [-ContentType <String[]>] [-Content <Object>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Array
```
New-PodeOAContentMediaType [-ContentType <String[]>] [-Content <Object>] [-Array] [-UniqueItems]
 [-MinItems <Int32>] [-MaxItems <Int32>] [-Title <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Upload
```
New-PodeOAContentMediaType [-ContentType <String[]>] [-Content <Object>] [-Upload] [-ContentEncoding <String>]
 [-PartContentMediaType <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The New-PodeOAContentMediaType function generates media content type definitions suitable for use in OpenAPI specifications.
It supports various media types and allows for the specification of content as either a single object or an array of objects.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeRoute -PassThru -Method get -Path '/pet/findByStatus' -Authentication 'Login-OAuth2' -Scope 'read' -ScriptBlock {
    Write-PodeJsonResponse -Value 'done' -StatusCode 200
} | Set-PodeOARouteInfo -Summary 'Finds Pets by status' -Description 'Multiple status values can be provided with comma separated strings' -Tags 'pet' -OperationId 'findPetsByStatus' -PassThru |
    Set-PodeOARequest -PassThru -Parameters @(
        (New-PodeOAStringProperty -Name 'status' -Description 'Status values that need to be considered for filter' -Default 'available' -Enum @('available', 'pending', 'sold') | ConvertTo-PodeOAParameter -In Query)
    ) |
    Add-PodeOAResponse -StatusCode 200 -Description 'Successful operation' -Content (New-PodeOAContentMediaType -ContentType 'application/json','application/xml' -Content 'Pet' -Array -UniqueItems) -PassThru |
    Add-PodeOAResponse -StatusCode 400 -Description 'Invalid status value'
This example demonstrates the use of New-PodeOAContentMediaType in defining a GET route '/pet/findByStatus' in an OpenAPI specification. The route includes request parameters and responses with media content types for 'application/json' and 'application/xml'.
```

### EXAMPLE 2
```
$content = [ordered]@{ type = 'string' }
$mediaType = 'application/json'
New-PodeOAContentMediaType -ContentType $mediaType -Content $content
This example creates a media content type definition for 'application/json' with a simple string content type.
```

### EXAMPLE 3
```
$content = [ordered]@{ type = 'object'; properties = [ordered]@{ name = @{ type = 'string' } } }
$mediaTypes = 'application/json', 'application/xml'
New-PodeOAContentMediaType -ContentType $mediaTypes -Content $content -Array -MinItems 1 -MaxItems 5 -Title 'UserList'
This example demonstrates defining an array of objects for both 'application/json' and 'application/xml' media types, with a specified range for the number of items and a title.
```

### EXAMPLE 4
```
Add-PodeRoute -PassThru -Method get -Path '/pet/findByStatus' -Authentication 'Login-OAuth2' -Scope 'read' -ScriptBlock {
    Write-PodeJsonResponse -Value 'done' -StatusCode 200
} | Set-PodeOARouteInfo -Summary 'Finds Pets by status' -Description 'Multiple status values can be provided with comma separated strings' -Tags 'pet' -OperationId 'findPetsByStatus' -PassThru |
    Set-PodeOARequest -PassThru -Parameters @(
        (New-PodeOAStringProperty -Name 'status' -Description 'Status values that need to be considered for filter' -Default 'available' -Enum @('available', 'pending', 'sold') | ConvertTo-PodeOAParameter -In Query)
    ) |
    Add-PodeOAResponse -StatusCode 200 -Description 'Successful operation' -Content (New-PodeOAContentMediaType -ContentType 'application/json','application/xml' -Content 'Pet' -Array -UniqueItems) -PassThru |
    Add-PodeOAResponse -StatusCode 400 -Description 'Invalid status value'
This example demonstrates the use of New-PodeOAContentMediaType in defining a GET route '/pet/findByStatus' in an OpenAPI specification. The route includes request parameters and responses with media content types for 'application/json' and 'application/xml'.
```

## PARAMETERS

### -Array
A switch parameter, used in the 'Array' parameter set, to indicate that the content should be treated as an array.

```yaml
Type: SwitchParameter
Parameter Sets: Array
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Content
The content definition for the media type.
This could be an object representing the structure of the content expected for the specified media types.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentEncoding
Define the content encoding for upload (Default Binary)

```yaml
Type: String
Parameter Sets: Upload
Aliases:

Required: False
Position: Named
Default value: Binary
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentType
An array of strings specifying the media types to be defined.
Media types should conform to standard MIME types (e.g., 'application/json', 'image/png').
The function validates these media types against a regular expression to ensure they are properly formatted.

Alias: MediaType

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MediaType

Required: False
Position: Named
Default value: */*
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxItems
Used in the 'Array' parameter set to specify the maximum number of items that should be present in the array.

```yaml
Type: Int32
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinItems
Used in the 'Array' parameter set to specify the minimum number of items that should be present in the array.

```yaml
Type: Int32
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartContentMediaType
Define the content encoding for multipart upload

```yaml
Type: String
Parameter Sets: Upload
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

### -Title
Used in the 'Array' parameter set to provide a title for the array content.

```yaml
Type: String
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UniqueItems
A switch parameter, used in the 'Array' parameter set, to specify that items in the array should be unique.

```yaml
Type: SwitchParameter
Parameter Sets: Array
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Upload
If provided configure the media for an upload changing the result based on the OpenApi version

```yaml
Type: SwitchParameter
Parameter Sets: Upload
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Specialized.OrderedDictionary
## NOTES
This function is useful for dynamically creating media type specifications in OpenAPI documentation, providing flexibility in defining the expected content structure for different media types.

## RELATED LINKS
