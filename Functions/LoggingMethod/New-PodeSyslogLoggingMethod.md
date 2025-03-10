---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeSyslogLoggingMethod

## SYNOPSIS
Creates a new Syslog logging method in Pode.

## SYNTAX

### DataFormat (Default)
```
New-PodeSyslogLoggingMethod -Server <String> [-Port <Int16>] [-Transport <String>]
 [-TlsProtocol <SslProtocols>] [-SyslogProtocol <String>] [-Encoding <String>] [-SkipCertificateCheck]
 [-FailureAction <String>] [-DataFormat <String>] [-AsUTC] [-DefaultTag <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeSyslogLoggingMethod -Server <String> [-Port <Int16>] [-Transport <String>]
 [-TlsProtocol <SslProtocols>] [-SyslogProtocol <String>] [-Encoding <String>] [-SkipCertificateCheck]
 [-FailureAction <String>] [-ISO8601] [-AsUTC] [-DefaultTag <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This function sets up a logging method that sends log messages to a remote Syslog server.
It supports various Syslog protocols (RFC3164, RFC5424), transports (UDP, TCP, TLS), and encoding formats.
The function also allows for custom date formatting or ISO 8601 compliance and can skip certificate checks for TLS connections.

## EXAMPLES

### EXAMPLE 1
```
$logMethod = New-PodeSyslogLoggingMethod -Server '192.168.1.100' -Transport 'TCP' -SyslogProtocol 'RFC3164'
```

Creates a new Syslog logging method that sends logs to the Syslog server at 192.168.1.100 using TCP and RFC3164 format.

### EXAMPLE 2
```
$logMethod = New-PodeSyslogLoggingMethod -Server '192.168.1.100' -SyslogProtocol 'RFC5424' -ISO8601 -AsUTC
```

Creates a Syslog logging method that uses RFC5424 format with ISO 8601 date formatting and logs time in UTC.

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

### -Port
The port on the Syslog server to send logs to.
Defaults to 514.

```yaml
Type: Int16
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 514
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

### -Server
The Syslog server to send logs to.
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

### -SkipCertificateCheck
If set, skips certificate validation for TLS connections.

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

### -SyslogProtocol
The Syslog protocol to use for message formatting.
Supported values are RFC3164 and RFC5424.
Defaults to RFC5424.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: RFC5424
Accept pipeline input: False
Accept wildcard characters: False
```

### -TlsProtocol
The TLS protocol version to use if TLS transport is selected.
Defaults to TLS 1.3.

```yaml
Type: SslProtocols
Parameter Sets: (All)
Aliases:
Accepted values: None, Ssl2, Ssl3, Tls, Default, Tls11, Tls12, Tls13

Required: False
Position: Named
Default value: Tls13
Accept pipeline input: False
Accept wildcard characters: False
```

### -Transport
The transport protocol to use.
Supported values are UDP, TCP, and TLS.
Defaults to UDP.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: UDP
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Hashtable: Returns a hashtable containing the Syslog logging method configuration.
## NOTES

## RELATED LINKS
