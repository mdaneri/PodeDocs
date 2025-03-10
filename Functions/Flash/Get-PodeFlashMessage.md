---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Flash
schema: 2.0.0
---

# Get-PodeFlashMessage

## SYNOPSIS
Returns all flash messages stored against a name, and the clears the messages.

## SYNTAX

```
Get-PodeFlashMessage [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns all of the flash messages, as an array, currently stored for the name within the session.
Once retrieved, the messages are removed from storage.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeFlashMessage -Name 'error'
```

## PARAMETERS

### -Name
The name of the flash messages to return.

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

### System.Object[]
## NOTES

## RELATED LINKS
