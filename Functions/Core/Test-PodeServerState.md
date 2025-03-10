---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Test-PodeServerState

## SYNOPSIS
Tests whether the Pode server is in a specified state.

## SYNTAX

```
Test-PodeServerState [-State] <PodeServerState> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Test-PodeServerState\` function checks the current state of the Pode server
by calling \`Get-PodeServerState\` and comparing the result to the specified state.
The function returns \`$true\` if the server is in the specified state and \`$false\` otherwise.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeServerState -State 'Running'
```

Returns \`$true\` if the server is currently running, otherwise \`$false\`.

### EXAMPLE 2
```
Test-PodeServerState -State 'Suspended'
```

Returns \`$true\` if the server is fully suspended, otherwise \`$false\`.

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

### -State
Specifies the server state to test.
Allowed values are:
- \`Terminated\`: The server is not running, and the context is null.
- \`Terminating\`: The server is in the process of shutting down.
- \`Resuming\`: The server is resuming from a suspended state.
- \`Suspending\`: The server is in the process of entering a suspended state.
- \`Suspended\`: The server is fully suspended.
- \`Restarting\`: The server is restarting.
- \`Starting\`: The server is in the process of starting up.
- \`Running\`: The server is actively running.

```yaml
Type: PodeServerState
Parameter Sets: (All)
Aliases:
Accepted values: Terminated, Terminating, Resuming, Suspending, Suspended, Restarting, Starting, Running

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
This function is part of Pode's server state management utilities.
It relies on the \`Get-PodeServerState\` function to determine the current state.

## RELATED LINKS
