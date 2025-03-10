---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Invoke-PodeScriptBlock

## SYNOPSIS
Invokes a ScriptBlock.

## SYNTAX

```
Invoke-PodeScriptBlock [-ScriptBlock] <ScriptBlock> [[-Arguments] <Object>] [[-UsingVariables] <Object[]>]
 [-Scoped] [-Return] [-Splat] [-NoNewClosure] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Invokes a ScriptBlock, supplying optional arguments, splatting, and returning any optional values.

## EXAMPLES

### EXAMPLE 1
```
Invoke-PodeScriptBlock -ScriptBlock { Write-PodeHost 'Hello!' }
```

### EXAMPLE 2
```
Invoke-PodeScriptBlock -Arguments 'Morty' -ScriptBlock { /* logic */ }
```

## PARAMETERS

### -Arguments
Any arguments that should be supplied to the ScriptBlock.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoNewClosure
Don't create a new closure before invoking the ScriptBlock.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
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

### -Return
Return any values that the ScriptBlock may return.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scoped
Run the ScriptBlock in a scoped context.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptBlock
The ScriptBlock to invoke.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Splat
Spat the argument onto the ScriptBlock.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsingVariables
Optional array of "using-variable" values, which will be automatically prepended to any supplied Arguments when supplied to the ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
