---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Get-PodeServerState

## SYNOPSIS
Retrieves the current state of the Pode server.

## SYNTAX

```
Get-PodeServerState [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The Get-PodeServerState function evaluates the internal state of the Pode server based on the cancellation tokens available
in the $PodeContext.
The function determines if the server is running, terminating, restarting, suspending, resuming, or
in any other predefined state.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeServerState
```

Retrieves the current state of the Pode server and returns it as a string.

## PARAMETERS

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

### [string] - The state of the Pode server as one of the following values:
###            'Terminated', 'Terminating', 'Resuming', 'Suspending', 'Suspended', 'Restarting', 'Starting', 'Running'.
## NOTES

## RELATED LINKS
