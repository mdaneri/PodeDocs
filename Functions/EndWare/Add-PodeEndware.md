---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: EndWare
schema: 2.0.0
---

# Add-PodeEndware

## SYNOPSIS
Adds a ScriptBlock as Endware to run at the end of each web Request.

## SYNTAX

```
Add-PodeEndware [-ScriptBlock] <ScriptBlock> [[-ArgumentList] <Object[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Adds a ScriptBlock as Endware to run at the end of each web Request.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeEndware -ScriptBlock { /* logic */ }
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Endware's ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -ScriptBlock
The ScriptBlock to add.
It will be supplied the current web event.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
