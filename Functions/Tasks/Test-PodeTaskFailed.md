---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Tasks
schema: 2.0.0
---

# Test-PodeTaskFailed

## SYNOPSIS
Test if a running Task process has failed.

## SYNTAX

```
Test-PodeTaskFailed [-Process] <Hashtable> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Test if a running Task process has failed.

## EXAMPLES

### EXAMPLE 1
```
Invoke-PodeTask -Name 'Example1' | Test-PodeTaskFailed
```

## PARAMETERS

### -Process
The Task process to be check.
The process returned by either Invoke-PodeTask or Get-PodeTaskProcess.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Task

Required: True
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

### System.Boolean
## NOTES

## RELATED LINKS
