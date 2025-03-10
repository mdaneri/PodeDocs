---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Tasks
schema: 2.0.0
---

# Get-PodeTaskProcess

## SYNOPSIS
Get all Task Processes.

## SYNTAX

```
Get-PodeTaskProcess [[-Name] <String[]>] [[-Id] <String[]>] [[-State] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Get all Task Processes, with support for filtering.
These are the processes created when using Invoke-PodeTask.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeTaskProcess
```

### EXAMPLE 2
```
Get-PodeTaskProcess -Name 'TaskName'
```

### EXAMPLE 3
```
Get-PodeTaskProcess -Id 'TaskId'
```

### EXAMPLE 4
```
Get-PodeTaskProcess -State 'Running'
```

## PARAMETERS

### -Id
An optional ID of the Task process to filter by, can be one or more.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
An optional Name of the Task to filter by, can be one or more.

```yaml
Type: String[]
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

### -State
An optional State of the Task process to filter by, can be one or more.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: All
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
