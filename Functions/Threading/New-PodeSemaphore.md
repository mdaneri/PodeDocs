---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Threading
schema: 2.0.0
---

# New-PodeSemaphore

## SYNOPSIS
Create a new Semaphore.

## SYNTAX

```
New-PodeSemaphore [-Name] <String> [[-Count] <Int32>] [[-Scope] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Create a new Semaphore.

## EXAMPLES

### EXAMPLE 1
```
New-PodeSemaphore -Name 'SelfSemaphore'
```

### EXAMPLE 2
```
New-PodeSemaphore -Name 'LocalSemaphore' -Scope Local
```

### EXAMPLE 3
```
New-PodeSemaphore -Name 'GlobalSemaphore' -Count 3 -Scope Global
```

## PARAMETERS

### -Count
The number of threads to allow a hold on the Semaphore.
(Default: 1)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Semaphore.

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

### -Scope
The Scope of the Semaphore, can be either Self, Local, or Global.
(Default: Self)
Self: The current process, or child processes.
Local: All processes for the current login session on Windows, or the the same as Self on Unix.
Global: All processes on the system, across every session.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Self
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
