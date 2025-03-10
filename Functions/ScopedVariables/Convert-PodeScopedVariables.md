---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: ScopedVariables
schema: 2.0.0
---

# Convert-PodeScopedVariables

## SYNOPSIS
Converts Scoped Variables within a given ScriptBlock.

## SYNTAX

```
Convert-PodeScopedVariables [[-ScriptBlock] <ScriptBlock>] [[-PSSession] <SessionState>]
 [[-Exclude] <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Converts Scoped Variables within a given ScriptBlock, and returns the updated ScriptBlock back, including any
using-variable values that will need to be supplied as parameters to the ScriptBlock first.

## EXAMPLES

### EXAMPLE 1
```
$ScriptBlock, $usingVars = Convert-PodeScopedVariables -ScriptBlock $ScriptBlock -PSSession $PSCmdlet.SessionState
```

### EXAMPLE 2
```
$ScriptBlock = Convert-PodeScopedVariables -ScriptBlock $ScriptBlock -Exclude Session, Using
```

## PARAMETERS

### -Exclude
An optional array of one or more Scoped Variable Names to Exclude from converting.
(ie: Session, Using, or a Name from Add-PodeScopedVariable)

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
An optional SessionState object, used to retrieve using-variable values.
If not supplied, using-variable values will not be converted.

```yaml
Type: SessionState
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object[]
### System.Management.Automation.ScriptBlock
## NOTES

## RELATED LINKS
