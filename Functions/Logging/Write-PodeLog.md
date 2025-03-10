---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Write-PodeLog

## SYNOPSIS
Writes an object, exception, or custom message to a configured custom or built-in logging method.

## SYNTAX

### Message (Default)
```
Write-PodeLog [-Name <String>] [-Level <String>] -Message <String> [-Tag <String>] [-Category <ErrorCategory>]
 [-ThreadId <Int32>] [-SuppressErrorLog] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### InputObject
```
Write-PodeLog [-Name <String>] -InputObject <PSObject> [-Level <String>] [-Tag <String>]
 [-Category <ErrorCategory>] [-ThreadId <Int32>] [-SuppressErrorLog] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Exception
```
Write-PodeLog [-Name <String>] -Exception <Exception> [-CheckInnerException] [-Level <String>] [-Tag <String>]
 [-ThreadId <Int32>] [-SuppressErrorLog] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ErrorRecord
```
Write-PodeLog [-Name <String>] -ErrorRecord <ErrorRecord> [-Level <String>] [-Tag <String>] [-ThreadId <Int32>]
 [-SuppressErrorLog] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function writes an object, custom log message, or exception to a logging method in Pode.
It supports both custom and built-in logging methods, allowing structured logging with different log levels, messages, tags, and additional details like thread ID.
The logging method can be used to write errors, warnings, and informational logs in a structured manner, depending on the log level and source of the log.
Optionally, it can suppress reporting of errors to the error log if the same error is logged.

## EXAMPLES

### EXAMPLE 1
```
$object | Write-PodeLog -Name 'LogName'
```

### EXAMPLE 2
```
Write-PodeLog -Name 'CustomLog' -Level 'Error' -Message 'An error occurred.'
```

### EXAMPLE 3
```
try {
    # Some code that throws an exception
} catch {
    Write-PodeLog -Name 'Syslog' -Exception $_ -SuppressErrorLog
}
```

## PARAMETERS

### -Category
The category of the custom error message (Default: NotSpecified).

```yaml
Type: ErrorCategory
Parameter Sets: Message, InputObject
Aliases:
Accepted values: NotSpecified, OpenError, CloseError, DeviceError, DeadlockDetected, InvalidArgument, InvalidData, InvalidOperation, InvalidResult, InvalidType, MetadataError, NotImplemented, NotInstalled, ObjectNotFound, OperationStopped, OperationTimeout, SyntaxError, ParserError, PermissionDenied, ResourceBusy, ResourceExists, ResourceUnavailable, ReadError, WriteError, FromStdErr, SecurityError, ProtocolError, ConnectionError, AuthenticationError, LimitsExceeded, QuotaExceeded, NotEnabled

Required: False
Position: Named
Default value: NotSpecified
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckInnerException
If specified, any inner exceptions of the provided exception are also logged.

```yaml
Type: SwitchParameter
Parameter Sets: Exception
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorRecord
The error record to log.
This is used when handling errors through PowerShell's error handling mechanism.

```yaml
Type: ErrorRecord
Parameter Sets: ErrorRecord
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Exception
An exception object to log.
Required for the 'Exception' parameter set.

```yaml
Type: Exception
Parameter Sets: Exception
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InputObject
The object to write to the logging method.
This is the default parameter set.

```yaml
Type: PSObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Level
The log level for the custom logging method (Default: 'Informational').
Log levels include 'Informational', 'Warning', 'Error', etc.

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

### -Message
The log message for the custom logging method.
Required for custom logging.

```yaml
Type: String
Parameter Sets: Message
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the logging method (e.g., 'Console', 'File', 'Syslog').

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

### -SuppressErrorLog
A switch to suppress writing the error to the error log if it has already been logged by this function.
Useful to prevent duplicate error logging.

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

### -Tag
A string that identifies the source application, service, or process generating the log message.
The tag helps distinguish log messages from different sources, making it easier to filter and analyze logs.
Default is '-'.

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

### -ThreadId
The ID of the thread where the log entry is generated.
If not specified, the current thread ID will be used.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
