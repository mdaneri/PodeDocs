---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeFileLoggingMethod

## SYNOPSIS
Creates a new file-based logging method in Pode.

## SYNTAX

### DataFormat (Default)
```
New-PodeFileLoggingMethod [-Path <String>] -Name <String> [-Format <String>] [-Separator <String>]
 [-MaxLength <Int32>] [-MaxDays <Int32>] [-MaxSize <Int32>] [-FailureAction <String>] [-DataFormat <String>]
 [-Encoding <String>] [-AsUTC] [-DefaultTag <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeFileLoggingMethod [-Path <String>] -Name <String> [-Format <String>] [-Separator <String>]
 [-MaxLength <Int32>] [-MaxDays <Int32>] [-MaxSize <Int32>] [-FailureAction <String>] [-Encoding <String>]
 [-ISO8601] [-AsUTC] [-DefaultTag <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function sets up a logging method that outputs log messages to a file.
It supports configuring log file paths, names, formats, sizes, and retention policies, along with various log formatting options such as custom date formats or ISO 8601.

## EXAMPLES

### EXAMPLE 1
```
$logMethod = New-PodeFileLoggingMethod -Path './logs' -Name 'requests'
```

Creates a new file logging method that stores logs in the './logs' directory with the base name 'requests'.

### EXAMPLE 2
```
$logMethod = New-PodeFileLoggingMethod -Name 'requests' -MaxDays 7 -MaxSize 100MB
```

Creates a file logging method that keeps logs for 7 days and creates new files once the log file reaches 100MB in size.

## PARAMETERS

### -AsUTC
If set, logs the time in UTC instead of the local time.

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

### -DataFormat
The custom date format for log entries.
Mutually exclusive with ISO8601.

```yaml
Type: String
Parameter Sets: DataFormat
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultTag
The tag to use if none is specified on the log entry.
Defaults to '-'.

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

### -Encoding
The encoding to use for Syslog messages.
Supported values are ASCII, BigEndianUnicode, Default, Unicode, UTF32, UTF7, and UTF8.
Defaults to UTF8.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: UTF8
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailureAction
Specifies the action to take if logging fails.
Options are: Ignore, Report, Halt (Default: Ignore).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Ignore
Accept pipeline input: False
Accept wildcard characters: False
```

### -Format
The format of the log entries.
Supported options are: RFC3164, RFC5424, Simple, and Default (Default: Default).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -ISO8601
If set, uses the ISO 8601 date format for log entries.
Mutually exclusive with DataFormat.

```yaml
Type: SwitchParameter
Parameter Sets: ISO8601
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxDays
The maximum number of days to keep log files.
Logs older than this will be removed automatically.
Defaults to 0 (no automatic removal).

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

### -MaxLength
The maximum length of log entries.
Defaults to -1 (no limit).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSize
The maximum size of a log file in bytes.
Once this size is exceeded, a new log file will be created.
Defaults to 0 (no size limit).

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

### -Name
The base name for the log files.
This parameter is mandatory.

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

### -Path
The file path where the logs will be stored.
Defaults to './logs'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: ./logs
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

### -Separator
The character(s) used to separate log fields in each entry.
Defaults to a space (' ').

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Hashtable: Returns a hashtable containing the logging method configuration.
## NOTES

## RELATED LINKS
