---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Start-PodeStopwatch

## SYNOPSIS
Starts a Stopwatch on some ScriptBlock, and outputs the duration at the end.

## SYNTAX

```
Start-PodeStopwatch -Name <String> [-ScriptBlock] <ScriptBlock> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Starts a Stopwatch on some ScriptBlock, and outputs the duration at the end.

## EXAMPLES

### EXAMPLE 1
```
Start-PodeStopwatch -Name 'ReadFile' -ScriptBlock { $content = Get-Content './file.txt' }
```

## PARAMETERS

### -Name
The name of the Stopwatch.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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
The ScriptBlock to time.

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
