---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Service
schema: 2.0.0
---

# Start-PodeService

## SYNOPSIS
Start a Pode-based service on Windows, Linux, or macOS.

## SYNTAX

### Default (Default)
```
Start-PodeService -Name <String> [-Agent] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Async
```
Start-PodeService -Name <String> [-Async] [-Timeout <Int32>] [-Agent] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
The \`Start-PodeService\` function ensures that a specified Pode-based service is running.
If the service is not registered or fails to start, the function throws an error.
It supports platform-specific service management commands:
- Windows: Uses \`sc.exe\`.
- Linux: Uses \`systemctl\`.
- macOS: Uses \`launchctl\`.

## EXAMPLES

### EXAMPLE 1
```
Start-PodeService -Name 'MyService'
```

Starts the service named 'MyService' if it is not already running.

### EXAMPLE 2
```
Start-PodeService -Name 'MyService' -Async
```

Starts the service named 'MyService' and returns immediately.

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
Indicates whether to return immediately after issuing the start command.
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
The name of the service to start.

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
- This function checks for necessary administrative/root privileges before execution.
- Service state management behavior:
	- If the service is already running, no action is taken.
	- If the service is not registered, an error is thrown.
- Service name is retrieved from the \`srvsettings.json\` file if available.
- Platform-specific commands are invoked to manage service states:
	- Windows: \`sc.exe start\`.
	- Linux: \`sudo systemctl start\`.
	- macOS: \`sudo launchctl start\`.
- Errors and logs are captured for debugging purposes.

## RELATED LINKS
