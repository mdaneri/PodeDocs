---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Tasks
schema: 2.0.0
---

# Add-PodeTask

## SYNOPSIS
Adds a new Task.

## SYNTAX

### Script (Default)
```
Add-PodeTask -Name <String> -ScriptBlock <ScriptBlock> [-ArgumentList <Hashtable>] [-Timeout <Int32>]
 [-TimeoutFrom <String>] [-MaxRetries <Int32>] [-RetryDelay <Int32>] [-AutoRetry]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodeTask -Name <String> -FilePath <String> [-ArgumentList <Hashtable>] [-Timeout <Int32>]
 [-TimeoutFrom <String>] [-MaxRetries <Int32>] [-RetryDelay <Int32>] [-AutoRetry]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a new Task, which can be asynchronously or synchronously invoked.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeTask -Name 'Example1' -ScriptBlock { Invoke-SomeLogic }
```

### EXAMPLE 2
```
Add-PodeTask -Name 'Example1' -ScriptBlock { return Get-SomeObject }
```

### EXAMPLE 3
```
Add-PodeTask -Name 'Example1' -ScriptBlock { return Get-SomeObject } -MaxRetries 3 -RetryDelay 5 -AutoRetry
```

## PARAMETERS

### -ArgumentList
A hashtable of arguments to supply to the Task's ScriptBlock.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoRetry
If supplied, the Task will automatically retry processes if they fail.

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

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the Task's logic.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxRetries
The maximum number of retries to attempt if the Task fails.
(Default: 0)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Task.

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

### -RetryDelay
The delay, in minutes, between automatically retrying failed task processes.
(Default: 0)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptBlock
The script for the Task.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: True
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

### -TimeoutFrom
Where to start the Timeout from, either 'Create', 'Start'.
(Default: 'Create')

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Create
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
