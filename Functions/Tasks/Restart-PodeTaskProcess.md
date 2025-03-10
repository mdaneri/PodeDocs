---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Tasks
schema: 2.0.0
---

# Restart-PodeTaskProcess

## SYNOPSIS
Restart a Task process which has failed.

## SYNTAX

```
Restart-PodeTaskProcess [-Process] <Hashtable> [-Timeout <Int32>] [-Wait] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Restart a Task process which has failed.

## EXAMPLES

### EXAMPLE 1
```
$task = Invoke-PodeTask -Name 'Example1' -Wait
if (Test-PodeTaskFailed -Process $task) {
    Restart-PodeTaskProcess -Process $task
}
```

### EXAMPLE 2
```
Get-PodeTaskProcess -State 'Failed' | ForEach-Object { Restart-PodeTaskProcess -Process $_ }
```

## PARAMETERS

### -Process
The Task process to be restarted.
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

### -Timeout
A Timeout, in seconds, to abort running the Task process.
(Default: -1 \[never timeout\])

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wait
If supplied, Pode will wait until the Task process has finished

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
