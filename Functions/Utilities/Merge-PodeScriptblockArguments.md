---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Merge-PodeScriptblockArguments

## SYNOPSIS
Merges Arguments and Using Variables together.

## SYNTAX

```
Merge-PodeScriptblockArguments [[-ArgumentList] <Object[]>] [[-UsingVariables] <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Merges Arguments and Using Variables together to be supplied to a ScriptBlock.
The Using Variables will be prepended so then are supplied first to a ScriptBlock.

## EXAMPLES

### EXAMPLE 1
```
$Arguments = @(Merge-PodeScriptblockArguments -ArgumentList $Arguments -UsingVariables $UsingVariables)
```

### EXAMPLE 2
```
$Arguments = @(Merge-PodeScriptblockArguments -UsingVariables $UsingVariables)
```

## PARAMETERS

### -ArgumentList
And optional array of Arguments.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -UsingVariables
And optional array of "using-variable" values to be prepended.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object[]
## NOTES

## RELATED LINKS
