---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeGraylogLoggingMethod

## SYNOPSIS
Configures logging to Graylog.

## SYNTAX

### DataFormat
```
New-PodeGraylogLoggingMethod -BaseUrl <String> [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC]
 [-DefaultTag <String>] [-DataFormat <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeGraylogLoggingMethod -BaseUrl <String> [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC]
 [-DefaultTag <String>] [-ISO8601] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`New-PodeGraylogLoggingMethod\` function sets up logging for Graylog, sending log entries to the Graylog server using GELF (Graylog Extended Log Format) over HTTP.

## EXAMPLES

### EXAMPLE 1
```
New-PodeGraylogLoggingMethod -BaseUrl 'http://graylog-server:12201/gelf'
```

Configures Graylog logging using the specified base URL.

## PARAMETERS

### -AsUTC
If present, converts timestamps to UTC.

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

### -BaseUrl
The base URL for the Graylog API, typically \`http://\<GRAYLOG_SERVER_IP\>:12201/gelf\`.

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
Sets a default tag for log entries.
Defaults to \`-\`.

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

### -FailureAction
Specifies the action to take if the logging request fails.
Valid values are \`Ignore\`, \`Report\`, and \`Halt\`.
The default is \`Ignore\`.

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

### -SkipCertificateCheck
If present, skips SSL certificate validation when sending logs.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable
## NOTES
This function sends logs to Graylog using GELF, which allows for structured logging.

## RELATED LINKS
