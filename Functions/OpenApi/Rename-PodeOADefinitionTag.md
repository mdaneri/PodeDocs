---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Rename-PodeOADefinitionTag

## SYNOPSIS
Renames an existing OpenAPI definition tag in Pode.

## SYNTAX

```
Rename-PodeOADefinitionTag [[-Tag] <String>] [-NewTag] <String> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This function renames an existing OpenAPI definition tag to a new tag name.
If the specified tag is the default definition tag, it updates the default tag as well.
It ensures that the new tag name does not already exist and that the function is not used within a Select-PodeOADefinition ScriptBlock.

## EXAMPLES

### EXAMPLE 1
```
Rename-PodeOADefinitionTag -Tag 'oldTag' -NewTag 'newTag'
```

Rename a specific OpenAPI definition tag

### EXAMPLE 2
```
Rename-PodeOADefinitionTag -NewTag 'newDefaultTag'
```

Rename the default OpenAPI definition tag

## PARAMETERS

### -NewTag
The new tag name for the OpenAPI definition.
This parameter is mandatory.

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

### -Tag
The current tag name of the OpenAPI definition.
If not specified, the default definition tag is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
This function will throw an error if:
- It is used inside a Select-PodeOADefinition ScriptBlock.
- The new tag name already exists.
- The current tag name does not exist.

## RELATED LINKS
