---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Service
schema: 2.0.0
---

# Register-PodeService

## SYNOPSIS
Registers a new Pode-based PowerShell worker as a service on Windows, Linux, or macOS.

## SYNTAX

```
Register-PodeService [-Name] <String> [[-Description] <String>] [[-DisplayName] <String>]
 [[-StartupType] <String>] [[-SecurityDescriptorSddl] <String>] [[-ParameterString] <String>]
 [-LogServicePodeHost] [[-ShutdownWaitTimeMs] <Int32>] [[-StartMaxRetryCount] <Int32>]
 [[-StartRetryDelayMs] <Int32>] [[-WindowsUser] <String>] [[-LinuxUser] <String>] [-Start] [-Agent]
 [[-Password] <SecureString>] [[-SettingsPath] <String>] [[-LogPath] <String>] [[-LogLevel] <String>]
 [[-LogMaxFileSize] <Int64>] [[-ConfigFile] <String>] [-IgnoreServerConfig]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Register-PodeService\` function configures and registers a Pode-based service that runs a PowerShell worker across multiple platforms
(Windows, Linux, macOS).
It creates the service with parameters such as paths to the worker script, log files, and service-specific settings.
A \`srvsettings.json\` configuration file is generated, and the service can be optionally started after registration.

## EXAMPLES

### EXAMPLE 1
```
Register-PodeService -Name "PodeExampleService" -Description "Example Pode Service" -ParameterString "-Verbose"
```

This example registers a Pode service named "PodeExampleService" with verbose logging enabled.

## PARAMETERS

### -Agent
Create an Agent instead of a Daemon on macOS (macOS only).

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
Position: 17
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A brief description of the service.
Defaults to "This is a Pode service."

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: This is a Pode service.
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Specifies the display name for the service (Windows only).
Defaults to "Pode Service($Name)".

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: "Pode Service($Name)"
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

### -LinuxUser
Specifies the username under which the service will run on Linux.
Defaults to the current user if not provided.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogLevel
Specifies the log verbosity level.
Valid values are 'Debug', 'Info', 'Warn', 'Error', or 'Critical'.
Defaults to 'Info'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: Info
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogMaxFileSize
Specifies the maximum size of the log file in bytes.
Defaults to 10 MB (10,485,760 bytes).

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 16
Default value: 10485760
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogPath
Specifies the path for the service log files.
If not provided, a default log directory is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogServicePodeHost
Enables logging for the Pode service host.
If not provided, the service runs in quiet mode.

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

### -Name
Specifies the name of the service to be registered.
This is a required parameter.

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

### -ParameterString
Any additional parameters to pass to the worker script when the service is run.
Defaults to an empty string.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
A secure password for the service account (Windows only).
If omitted, the service account defaults to 'NT AUTHORITY\SYSTEM'.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
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

### -SecurityDescriptorSddl
A security descriptor in SDDL format, specifying the permissions for the service (Windows only).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingsPath
Specifies the directory to store the service configuration file (\`\<name\>_svcsettings.json\`).
If not provided, a default directory is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShutdownWaitTimeMs
Maximum time in milliseconds to wait for the service to shut down gracefully before forcing termination.
Defaults to 30,000 milliseconds (30 seconds).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 30000
Accept pipeline input: False
Accept wildcard characters: False
```

### -Start
A switch to start the service immediately after registration.

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

### -StartMaxRetryCount
The maximum number of retries to start the PowerShell process before giving up.
Default is 3 retries.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: 3
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRetryDelayMs
The delay (in milliseconds) between retry attempts to start the PowerShell process.
Default is 5,000 milliseconds (5 seconds).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: 5000
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartupType
Specifies the startup type of the service ('Automatic' or 'Manual').
Defaults to 'Automatic'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsUser
Specifies the username under which the service will run on Windows.
Defaults to the current user if not provided.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
- Supports cross-platform service registration on Windows, Linux, and macOS.
- Generates a \`srvsettings.json\` file with service-specific configurations.
- Automatically starts the service using the \`-Start\` switch after registration.
- Dynamically obtains the PowerShell executable path for compatibility across platforms.

## RELATED LINKS
