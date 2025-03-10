---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Write-PodeErrorLog

## SYNOPSIS
Logs an Exception, ErrorRecord, or a custom error message using Pode's built-in logging mechanism.

## SYNTAX

### Exception
```
Write-PodeErrorLog -Exception <Exception> [-Level <String>] [-CheckInnerException] [-ThreadId <Int32>]
 [-Tag <String>] [-SuppressDefaultLog] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ErrorRecord
```
Write-PodeErrorLog -ErrorRecord <ErrorRecord> [-Level <String>] [-ThreadId <Int32>] [-Tag <String>]
 [-SuppressDefaultLog] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function logs exceptions, error records, or custom error messages with optional error categories and levels.
It can also log inner exceptions and associate the error with a specific thread ID.
Error levels can be set, and inner exceptions can be checked for more detailed logging.

## EXAMPLES

### EXAMPLE 1
```
try {
    # Some operation
} catch {
    $_ | Write-PodeErrorLog
}
```

### EXAMPLE 2
```
[System.Exception]::new('Custom error message') | Write-PodeErrorLog -CheckInnerException
```

## PARAMETERS

### -CheckInnerException
If specified, logs any inner exceptions associated with the provided exception.

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
The exception object to log.
This is used when logging caught exceptions.

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

### -Level
The logging level for the error.
Supported levels are: Error, Warning, Informational, Verbose, Debug (Default: Error).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Error
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

### -SuppressDefaultLog
A switch to suppress writing the error to the default log.

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
Default value: -
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreadId
The ID of the thread where the error occurred.
If not specified, the current thread's ID is used.

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
