---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeTerminalLoggingMethod

## SYNOPSIS
Creates a new terminal logging method in Pode.

## SYNTAX

### DataFormat (Default)
```
New-PodeTerminalLoggingMethod [-DataFormat <String>] [-AsUTC] [-DefaultTag <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeTerminalLoggingMethod [-ISO8601] [-AsUTC] [-DefaultTag <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This function sets up a logging method that outputs log messages to the terminal using Pode's internal terminal logging logic.
It allows specifying a custom date format, or uses the ISO 8601 format if requested.
Additionally, it supports logging time in UTC.

## EXAMPLES

### EXAMPLE 1
```
$logMethod = New-PodeTerminalLoggingMethod -DataFormat 'yyyy/MM/dd HH:mm:ss'
```

Creates a terminal logging method using the specified custom date format.

### EXAMPLE 2
```
$logMethod = New-PodeTerminalLoggingMethod -ISO8601 -AsUTC
```

Creates a terminal logging method that logs messages using the ISO 8601 date format and logs the time in UTC.

## PARAMETERS

### -AsUTC
If set, the time will be logged in UTC instead of local time.

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
The custom date format to use for log entries.
If not provided, a default format of 'dd/MMM/yyyy:HH:mm:ss zzz' is used.
This parameter is mutually exclusive with the ISO8601 parameter.

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

### -ISO8601
If set, the date format will follow ISO 8601 (equivalent to -DataFormat 'yyyy-MM-ddTHH:mm:ssK').
This parameter is mutually exclusive with the DataFormat parameter.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Hashtable: Returns a hashtable containing the logging method configuration.
## NOTES

## RELATED LINKS
