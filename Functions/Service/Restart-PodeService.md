---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Service
schema: 2.0.0
---

# Restart-PodeService

## SYNOPSIS
Restart a Pode service on Windows, Linux, or macOS by sending the appropriate restart signal.

## SYNTAX

### Default (Default)
```
Restart-PodeService -Name <String> [-Agent] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Async
```
Restart-PodeService -Name <String> [-Async] [-Timeout <Int32>] [-Agent] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
The \`Restart-PodeService\` function handles the restart operation for a Pode service across multiple platforms:
- Windows: Sends a restart control signal (128) using \`sc.exe control\`.
- Linux/macOS: Sends the \`SIGHUP\` signal to the service's process ID.

## EXAMPLES

### EXAMPLE 1
```
Restart-PodeService -Name "MyPodeService"
```

Attempts to restart the Pode service named "MyPodeService" on the current platform.

### EXAMPLE 2
```
Restart-PodeService -Name "AnotherService" -Verbose
```

Restarts the Pode service named "AnotherService" with detailed verbose output.

## PARAMETERS

### -Agent
Specifies that only agent-type services should be returned.
This parameter is applicable to macOS only.

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

### -Async
Indicates whether to return immediately after issuing the restart command.
If not specified, the function waits until the service reaches the 'Running' state.

```yaml
Type: SwitchParameter
Parameter Sets: Async
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the Pode service to restart.

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

### -Timeout
The maximum time, in seconds, to wait for the service to reach the 'Running' state when not using \`-Async\`.
Defaults to 10 seconds.

```yaml
Type: Int32
Parameter Sets: Async
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Boolean
## NOTES
- This function requires administrative/root privileges to execute.
- Platform-specific behavior:
	- Windows: Uses \`sc.exe control\` with the signal \`128\` to restart the service.
	- Linux/macOS: Sends the \`SIGHUP\` signal to the service process.
- If the service is not running or suspended, no restart signal is sent.
- If the service is not registered, an error is thrown.
- Errors and logs are captured for debugging purposes.

## RELATED LINKS
