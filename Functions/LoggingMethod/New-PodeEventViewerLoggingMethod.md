---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeEventViewerLoggingMethod

## SYNOPSIS
Creates a new Event Viewer logging method in Pode.

## SYNTAX

### DataFormat (Default)
```
New-PodeEventViewerLoggingMethod [-EventLogName <String>] [-Source <String>] [-EventID <Int32>]
 [-FailureAction <String>] [-DataFormat <String>] [-AsUTC] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### ISO8601
```
New-PodeEventViewerLoggingMethod [-EventLogName <String>] [-Source <String>] [-EventID <Int32>]
 [-FailureAction <String>] [-ISO8601] [-AsUTC] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function sets up a logging method that outputs log messages to the Windows Event Viewer.
It allows configuring the log name, source, and event ID, along with date formatting options like custom formats or ISO 8601.

## EXAMPLES

### EXAMPLE 1
```
$logMethod = New-PodeEventViewerLoggingMethod -EventLogName 'Application' -Source 'PodeApp'
```

Creates a new Event Viewer logging method that writes to the 'Application' log with the source 'PodeApp'.

### EXAMPLE 2
```
$logMethod = New-PodeEventViewerLoggingMethod -Source 'MyApp' -EventID 1001 -ISO8601
```

Creates a new Event Viewer logging method with ISO 8601 date format, writing to the 'MyApp' source and using event ID 1001.

## PARAMETERS

### -AsUTC
If set, logs the time in UTC instead of local time.

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

### -EventID
The ID of the event to log.
Defaults to 0.

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

### -EventLogName
The name of the event log to write to.
Defaults to 'Application'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Application
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

### -Source
The source of the log entries.
Defaults to 'Pode'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Pode
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
