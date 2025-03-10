---
external help file: Pode-help.xml
Module Name: Pode
online version: https://swagger.io/docs/specification/basic-structure/
PodeType: OAComponents
schema: 2.0.0
---

# Add-PodeOAComponentParameter

## SYNOPSIS
Adds a reusable component for a request parameter.

## SYNTAX

```
Add-PodeOAComponentParameter [-Name <String>] [-Parameter] <Hashtable> [-DefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a reusable component for a request parameter.

## EXAMPLES

### EXAMPLE 1
```
New-PodeOAIntProperty -Name 'userId' | ConvertTo-PodeOAParameter -In Query | Add-PodeOAComponentParameter -Name 'UserIdParam'
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The reference Name of the parameter.

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

### -Parameter
The Parameter to use for the component (from ConvertTo-PodeOAParameter)

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[https://swagger.io/docs/specification/basic-structure/](https://swagger.io/docs/specification/basic-structure/)

[https://swagger.io/docs/specification/data-models/](https://swagger.io/docs/specification/data-models/)

[https://swagger.io/docs/specification/describing-parameters/](https://swagger.io/docs/specification/describing-parameters/)

