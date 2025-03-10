---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OAComponents
schema: 2.0.0
---

# Remove-PodeOAComponent

## SYNOPSIS
Remove an OpenAPI component if exist

## SYNTAX

```
Remove-PodeOAComponent [-Field] <String> [-Name] <String> [[-DefinitionTag] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Remove an OpenAPI component if exist

## EXAMPLES

### EXAMPLE 1
```
Remove-PodeOAComponent -Field 'responses' -Name 'myresponse' -DefinitionTag 'default'
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
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Field
The component type

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

### -Name
The component Name

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
