---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Protect-PodeLogItem

## SYNOPSIS
Masks values within a log item to protect sensitive information.

## SYNTAX

```
Protect-PodeLogItem [[-Item] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Masks values within a log item, or any string, to protect sensitive information.
Patterns, and the Mask, can be configured via the server.psd1 configuration file.

## EXAMPLES

### EXAMPLE 1
```
$value = Protect-PodeLogItem -Item 'Username=Morty, Password=Hunter2'
```

## PARAMETERS

### -Item
The string Item to mask values.

```yaml
Type: String
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.String
## NOTES

## RELATED LINKS
