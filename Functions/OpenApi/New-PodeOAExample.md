---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# New-PodeOAExample

## SYNOPSIS
Creates a new OpenAPI example.

## SYNTAX

### Inbuilt (Default)
```
New-PodeOAExample [[-ParamsList] <OrderedDictionary>] [-ContentType <String>] -Name <String>
 [-Summary <String>] [-Description <String>] [-Value <Object>] [-ExternalValue <String>]
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Reference
```
New-PodeOAExample [[-ParamsList] <OrderedDictionary>] [-ContentType <String>] -Reference <String>
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new OpenAPI example.

## EXAMPLES

### EXAMPLE 1
```
New-PodeOAExample -ContentType 'text/plain' -Name 'user' -Summary = 'User Example in Plain text' -ExternalValue = 'http://foo.bar/examples/user-example.txt'
```

### EXAMPLE 2
```
$example =
    New-PodeOAExample -ContentType 'application/json' -Name 'user' -Summary = 'User Example' -ExternalValue = 'http://foo.bar/examples/user-example.json'  |
    New-PodeOAExample -ContentType 'application/xml' -Name 'user' -Summary = 'User Example in XML' -ExternalValue = 'http://foo.bar/examples/user-example.xml'
```

## PARAMETERS

### -ContentType
The Media Content Type associated with the Example.

Alias: MediaType

```yaml
Type: String
Parameter Sets: (All)
Aliases: MediaType

Required: False
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
Long description for the example.

```yaml
Type: String
Parameter Sets: Inbuilt
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalValue
A URL that points to the literal example.
This provides the capability to reference examples that cannot easily be included in JSON or YAML documents.
The -Value parameter and -ExternalValue parameter are mutually exclusive. 
|

```yaml
Type: String
Parameter Sets: Inbuilt
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Example.

```yaml
Type: String
Parameter Sets: Inbuilt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParamsList
Used to pipeline multiple properties

```yaml
Type: OrderedDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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
A reference to a reusable component example

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

### -Summary
Short description for the example

```yaml
Type: String
Parameter Sets: Inbuilt
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Embedded literal example.
The  value Parameter and ExternalValue parameter are mutually exclusive.
To represent examples of media types that cannot naturally represented in JSON or YAML, use a string value to contain the example, escaping where necessary.

```yaml
Type: Object
Parameter Sets: Inbuilt
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

### System.Collections.Specialized.OrderedDictionary
## NOTES

## RELATED LINKS
