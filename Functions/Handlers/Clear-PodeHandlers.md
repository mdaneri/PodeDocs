---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Handlers
schema: 2.0.0
---

# Clear-PodeHandlers

## SYNOPSIS
Removes all added Handlers, or Handlers of a specific Type.

## SYNTAX

```
Clear-PodeHandlers [[-Type] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Removes all added Handlers, or Handlers of a specific Type.

## EXAMPLES

### EXAMPLE 1
```
Clear-PodeHandlers -Type Smtp
```

## PARAMETERS

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

### -Type
The Type of Handlers to remove.

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

## RELATED LINKS
