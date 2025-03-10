---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeDatadogLoggingMethod

## SYNOPSIS
Configures logging to Datadog Logs.

## SYNTAX

### DataFormat
```
New-PodeDatadogLoggingMethod -ApiKey <String> -BaseUrl <String> [-FailureAction <String>]
 [-SkipCertificateCheck] [-AsUTC] [-DefaultTag <String>] [-DataFormat <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeDatadogLoggingMethod -ApiKey <String> -BaseUrl <String> [-FailureAction <String>]
 [-SkipCertificateCheck] [-AsUTC] [-DefaultTag <String>] [-ISO8601] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
The \`New-PodeDatadogLoggingMethod\` function sets up logging for Datadog, allowing log entries to be sent to Datadog's log intake endpoint using the provided API key.

## EXAMPLES

### EXAMPLE 1
```
New-PodeDatadogLoggingMethod -ApiKey 'my-datadog-api-key' -BaseUrl 'https://http-intake.logs.datadoghq.com/v1/input'
```

Configures Datadog logging using the provided API key and URL.

## PARAMETERS

### -ApiKey
The Datadog API key used to authenticate requests.

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
The Datadog intake URL, typically \`https://http-intake.logs.datadoghq.com/v1/input\`.

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
This function sends logs to Datadog Logs using a REST API call with the API key as authorization.

## RELATED LINKS
