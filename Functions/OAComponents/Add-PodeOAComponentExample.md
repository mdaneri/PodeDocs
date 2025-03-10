---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OAComponents
schema: 2.0.0
---

# Add-PodeOAComponentExample

## SYNOPSIS
Adds a reusable example component.

## SYNTAX

### Value (Default)
```
Add-PodeOAComponentExample -Name <String> [-Summary <String>] [-Description <String>] -Value <Object>
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ExternalValue
```
Add-PodeOAComponentExample -Name <String> [-Summary <String>] [-Description <String>] -ExternalValue <String>
 [-DefinitionTag <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a reusable example component.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAComponentExample -name 'frog-example' -Summary "An example of a frog with a cat's name" -Value @{name = 'Jaguar'; petType = 'Panthera'; color = 'Lion'; gender = 'Male'; breed = 'Mantella Baroni' }
```

## PARAMETERS

### -DefinitionTag
An Array of strings representing the unique tag for the API specification.
This tag helps in distinguishing between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with. 
|

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
Parameter Sets: (All)
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

```yaml
Type: String
Parameter Sets: ExternalValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Example.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Title

Required: True
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

### -Summary
Short description for the example

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

### -Value
Embedded literal example.
The  value Parameter and ExternalValue parameter are mutually exclusive.
To represent examples of media types that cannot naturally represented in JSON or YAML, use a string value to contain the example, escaping where necessary.

```yaml
Type: Object
Parameter Sets: Value
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
