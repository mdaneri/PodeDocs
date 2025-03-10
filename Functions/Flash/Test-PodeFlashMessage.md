---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Flash
schema: 2.0.0
---

# Test-PodeFlashMessage

## SYNOPSIS
Tests if there are any flash messages currently being stored for a supplied name.

## SYNTAX

```
Test-PodeFlashMessage [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Tests if there are any flash messages currently being stored for a supplied name.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeFlashMessage -Name 'error'
```

## PARAMETERS

### -Name
The name of the flash message to check.

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

### System.Boolean
## NOTES

## RELATED LINKS
