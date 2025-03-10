---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Tasks
schema: 2.0.0
---

# Wait-PodeTask

## SYNOPSIS
Waits for a Task process to finish, and returns a result if there is one.

## SYNTAX

```
Wait-PodeTask [-Process] <Object> [-Timeout <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Waits for a Task process to finish, and returns a result if there is one.

## EXAMPLES

### EXAMPLE 1
```
$context = Wait-PodeTask -Task $listener.GetContextAsync()
```

### EXAMPLE 2
```
$result = Invoke-PodeTask -Name 'Example1' | Wait-PodeTask
```

## PARAMETERS

### -Process
The Task process to wait on.
The process returned by either Invoke-PodeTask or Get-PodeTaskProcess.

```yaml
Type: Object
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
An optional Timeout in milliseconds.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
