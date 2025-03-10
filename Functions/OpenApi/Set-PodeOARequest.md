---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Set-PodeOARequest

## SYNOPSIS
Sets the OpenAPI request definition for a route.

## SYNTAX

```
Set-PodeOARequest [-Route] <Hashtable[]> [-Parameters <Hashtable[]>] [-RequestBody <Hashtable>] [-PassThru]
 [-AllowNonStandardBody] [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Configures the OpenAPI request properties for a specified route, including parameters and request body definition.
This function defines how the route should handle incoming requests in accordance with OpenAPI standards.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeRoute -PassThru | Set-PodeOARequest -RequestBody (New-PodeOARequestBody -Schema 'UserIdBody') -AllowNonStandardBody
```

Sets the request body for a route and allows non-standard HTTP methods like DELETE to use a request body.

## PARAMETERS

### -AllowNonStandardBody
Allows methods like DELETE and GET to include a request body, which is generally discouraged by RFC 7231.
This can be used to relax the default restriction and enable a body for HTTP methods that don't typically support it.

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

### -Parameters
Defines the parameters for the request, provided by ConvertTo-PodeOAParameter.

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

### -PassThru
If specified, returns the original route object for additional chaining after setting the request properties.

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

### -RequestBody
Specifies the body schema for the request, provided by New-PodeOARequestBody.

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

### -Route
The route to set a request definition for.
This is typically passed through from -PassThru on Add-PodeRoute.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable[]
## NOTES

## RELATED LINKS
