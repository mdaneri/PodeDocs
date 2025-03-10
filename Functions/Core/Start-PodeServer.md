---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Start-PodeServer

## SYNOPSIS
Starts a Pode server with the supplied script block or file containing the server logic.

## SYNTAX

### Script (Default)
```
Start-PodeServer [-ScriptBlock] <ScriptBlock> [-Interval <Int32>] [-Name <String>] [-Threads <Int32>]
 [-RootPath <String>] [-Request <Object>] [-ServerlessType <String>] [-StatusPageExceptions <String>]
 [-ListenerType <String>] [-EnablePool <String[]>] [-Browse] [-EnableBreakpoints] [-DisableTermination]
 [-Quiet] [-DisableConsoleInput] [-ClearHost] [-HideOpenAPI] [-HideEndpoints] [-ShowHelp] [-IgnoreServerConfig]
 [-ConfigFile <String>] [-ApplicationName <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ScriptDaemon
```
Start-PodeServer [-ScriptBlock] <ScriptBlock> [-Interval <Int32>] [-Name <String>] [-Threads <Int32>]
 [-RootPath <String>] [-Request <Object>] [-ServerlessType <String>] [-StatusPageExceptions <String>]
 [-ListenerType <String>] [-EnablePool <String[]>] [-ClearHost] [-HideOpenAPI] [-HideEndpoints] [-ShowHelp]
 [-IgnoreServerConfig] [-ConfigFile <String>] [-Daemon] [-ApplicationName <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### FileDaemon
```
Start-PodeServer -FilePath <String> [-Interval <Int32>] [-Name <String>] [-Threads <Int32>]
 [-RootPath <String>] [-Request <Object>] [-ServerlessType <String>] [-StatusPageExceptions <String>]
 [-ListenerType <String>] [-EnablePool <String[]>] [-CurrentPath] [-ClearHost] [-HideOpenAPI] [-HideEndpoints]
 [-ShowHelp] [-IgnoreServerConfig] [-ConfigFile <String>] [-Daemon] [-ApplicationName <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Start-PodeServer -FilePath <String> [-Interval <Int32>] [-Name <String>] [-Threads <Int32>]
 [-RootPath <String>] [-Request <Object>] [-ServerlessType <String>] [-StatusPageExceptions <String>]
 [-ListenerType <String>] [-EnablePool <String[]>] [-Browse] [-CurrentPath] [-EnableBreakpoints]
 [-DisableTermination] [-Quiet] [-DisableConsoleInput] [-ClearHost] [-HideOpenAPI] [-HideEndpoints] [-ShowHelp]
 [-IgnoreServerConfig] [-ConfigFile <String>] [-ApplicationName <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This function initializes and starts a Pode server based on the provided configuration.
It supports both inline script blocks and external files for defining server logic.
The server's behavior, console output, and various features can be customized using parameters.
Additionally, it manages server termination, cancellation, and cleanup processes.

## EXAMPLES

### EXAMPLE 1
```
Start-PodeServer { /* server logic */ }
Starts a Pode server using the supplied script block.
```

### EXAMPLE 2
```
Start-PodeServer -FilePath './server.ps1' -Browse
Starts a Pode server using the logic defined in an external file and opens the default endpoint in the browser.
```

### EXAMPLE 3
```
Start-PodeServer -ServerlessType AwsLambda -Request $LambdaInput { /* server logic */ }
Starts a Pode server in a serverless environment, using AWS Lambda input.
```

### EXAMPLE 4
```
Start-PodeServer -HideOpenAPI -ClearHost { /* server logic */ }
Starts a Pode server with console output configured to hide OpenAPI details and clear the console on state changes.
```

## PARAMETERS

### -ApplicationName
Specifies the name of the Pode application.
If not provided, the default is the script's file name (excluding the extension).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Browse
Opens the default web endpoint in the browser upon server start.

```yaml
Type: SwitchParameter
Parameter Sets: Script, File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearHost
Clears the console screen whenever the server state changes (e.g., running → suspend → resume).

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

### -ConfigFile
Specifies a custom configuration file instead of using the default \`server.psd1\`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CurrentPath
Sets the server's root path to the current working directory.
Only applicable when -FilePath is used.

```yaml
Type: SwitchParameter
Parameter Sets: FileDaemon
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Daemon
Configures the server to run as a daemon with minimal console interaction and output.

```yaml
Type: SwitchParameter
Parameter Sets: ScriptDaemon, FileDaemon
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableConsoleInput
Disables all console interactions for the server.

```yaml
Type: SwitchParameter
Parameter Sets: Script, File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableTermination
Prevents termination, suspension, or resumption of the server via console commands.

```yaml
Type: SwitchParameter
Parameter Sets: Script, File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableBreakpoints
Enables breakpoints created using \`Wait-PodeDebugger\`.

```yaml
Type: SwitchParameter
Parameter Sets: Script, File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePool
Configures specific runspace pools (e.g., Timers, Schedules, Tasks, WebSockets, Files) for ad-hoc usage.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
A literal or relative path to a file containing the server's logic.
The directory of this file will be used as the server's root path unless a specific -RootPath is supplied.

```yaml
Type: String
Parameter Sets: FileDaemon, File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HideEndpoints
Hides the list of active endpoints from the console output.

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

### -HideOpenAPI
Hides OpenAPI details such as specification and documentation URLs from the console output.

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

### -IgnoreServerConfig
Prevents the server from loading settings from the server.psd1 configuration file.

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

### -Interval
Specifies the interval in seconds for invoking the script block in 'Service' type servers.

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

### -ListenerType
Specifies a custom socket listener.
Defaults to Pode's inbuilt listener.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: [string]::Empty
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
An optional name for the server, useful for identification in logs and future extensions.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

### -Quiet
Suppresses all output from the server.

```yaml
Type: SwitchParameter
Parameter Sets: Script, File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Request
Provides request details for serverless environments that Pode can parse and use.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootPath
Overrides the server's root path.
If not provided, the root path will be derived from the file path or the current working directory.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptBlock
The main logic for the server, provided as a script block.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ScriptBlock
Parameter Sets: ScriptDaemon
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServerlessType
Specifies the serverless type for Pode.
Valid values are:
- AzureFunctions
- AwsLambda

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: [string]::Empty
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowHelp
Displays a help menu in the console with available control commands.

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

### -StatusPageExceptions
Controls the visibility of stack traces on status pages.
Valid values are:
- Show
- Hide

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: [string]::Empty
Accept pipeline input: False
Accept wildcard characters: False
```

### -Threads
The number of threads to allocate for Web, SMTP, and TCP servers.
Defaults to 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
This function is part of the Pode framework and is responsible for server initialization, configuration,
request handling, and cleanup.
It supports both standalone and serverless deployments, and provides
extensive customization options for developers.

## RELATED LINKS
