---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeGoogleLoggingMethod

## SYNOPSIS
Configures logging to Google Cloud Logging.

## SYNTAX

### DataFormat
```
New-PodeGoogleLoggingMethod -ProjectId <String> -AccessToken <String> [-LogName <String>]
 [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC] [-DefaultTag <String>] [-DataFormat <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeGoogleLoggingMethod -ProjectId <String> -AccessToken <String> [-LogName <String>]
 [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC] [-DefaultTag <String>] [-ISO8601]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`New-PodeGoogleLoggingMethod\` function sets up logging for Google Cloud Logging, allowing log entries to be sent to Google Cloud using the project ID and access token for authentication.

## EXAMPLES

### EXAMPLE 1
```
New-PodeGoogleLoggingMethod -ProjectId 'my-project-id' -AccessToken 'ya29.a0AfH6SM...' -LogName 'ApplicationLogs'
```

Sets up Google Cloud Logging with the specified project ID and access token.

## PARAMETERS

### -AccessToken
OAuth 2.0 access token for authenticating with Google Cloud.

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

### -LogName
The name of the log in Google Cloud Logging.
Defaults to \`default_log\`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Default_log
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

### -ProjectId
The Google Cloud Project ID.

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
This function sends log entries to Google Cloud Logging using the Google Cloud Logging REST API, allowing for structured logging within a specific project.

## RELATED LINKS
