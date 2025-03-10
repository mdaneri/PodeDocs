---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: State
schema: 2.0.0
---

# Remove-PodeState

## SYNOPSIS
Removes some state object from the shared state.

## SYNTAX

```
Remove-PodeState [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Removes some state object from the shared state.
After removal, the original object being stored is returned.

## EXAMPLES

### EXAMPLE 1
```
Remove-PodeState -Name 'Data'
```

## PARAMETERS

### -Name
The name of the state object.

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

## NOTES

## RELATED LINKS
