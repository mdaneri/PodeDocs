---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: ScopedVariables
schema: 2.0.0
---

# Convert-PodeScopedVariable

## SYNOPSIS
Converts a Scoped Variable within a given ScriptBlock.

## SYNTAX

```
Convert-PodeScopedVariable [-Name] <String> [[-ScriptBlock] <ScriptBlock>] [[-PSSession] <SessionState>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Converts a Scoped Variable within a given ScriptBlock, and returns the updated ScriptBlock back, including any
other values that will need to be supplied as parameters to the ScriptBlock first.

## EXAMPLES

### EXAMPLE 1
```
$ScriptBlock = Convert-PodeScopedVariable -Name State -ScriptBlock $ScriptBlock
```

### EXAMPLE 2
```
$ScriptBlock, $otherResults = Convert-PodeScopedVariable -Name Using -ScriptBlock $ScriptBlock
```

## PARAMETERS

### -Name
The Name of the Scoped Variable to convert.
(ie: Session, Using, or a Name from Add-PodeScopedVariable)

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

### -PSSession
An optional SessionState object, used to retrieve using-variable values or other values where scope is required.

```yaml
Type: SessionState
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptBlock
The ScriptBlock to be converted.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Management.Automation.ScriptBlock
## NOTES

## RELATED LINKS
