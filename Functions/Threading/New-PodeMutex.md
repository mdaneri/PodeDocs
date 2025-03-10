---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Threading
schema: 2.0.0
---

# New-PodeMutex

## SYNOPSIS
Create a new Mutex.

## SYNTAX

```
New-PodeMutex [-Name] <String> [[-Scope] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Create a new Mutex.

## EXAMPLES

### EXAMPLE 1
```
New-PodeMutex -Name 'SelfMutex'
```

### EXAMPLE 2
```
New-PodeMutex -Name 'LocalMutex' -Scope Local
```

### EXAMPLE 3
```
New-PodeMutex -Name 'GlobalMutex' -Scope Global
```

## PARAMETERS

### -Name
The Name of the Mutex.

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
The Scope of the Mutex, can be either Self, Local, or Global.
(Default: Self)
Self: The current process, or child processes.
Local: All processes for the current login session on Windows, or the the same as Self on Unix.
Global: All processes on the system, across every session.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
