---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Test-PodeOADefinition

## SYNOPSIS
Validate the OpenAPI definition if all Reference are satisfied

## SYNTAX

```
Test-PodeOADefinition [[-DefinitionTag] <String[]>]
```

## DESCRIPTION
Validate the OpenAPI definition if all Reference are satisfied

## EXAMPLES

### EXAMPLE 1
```
if ((Test-PodeOADefinition -DefinitionTag 'v3').count -eq 0){
    Write-PodeHost "The OpenAPI definition is valid"
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
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
