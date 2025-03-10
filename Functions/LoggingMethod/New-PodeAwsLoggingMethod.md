---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeAwsLoggingMethod

## SYNOPSIS
Configures logging to AWS CloudWatch Logs.

## SYNTAX

### DataFormat
```
New-PodeAwsLoggingMethod -BaseUrl <String> -Region <String> -LogGroupName <String> -LogStreamName <String>
 -AuthorizationHeader <String> [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC]
 [-DefaultTag <String>] [-DataFormat <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeAwsLoggingMethod -BaseUrl <String> -Region <String> -LogGroupName <String> -LogStreamName <String>
 -AuthorizationHeader <String> [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC]
 [-DefaultTag <String>] [-ISO8601] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`New-PodeAwsLoggingMethod\` function configures a logging method for AWS CloudWatch Logs.
It initializes a logging queue and sends log events to AWS CloudWatch using the specified log group and stream names.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAwsLoggingMethod -BaseUrl 'https://logs.us-east-1.amazonaws.com' -Region 'us-east-1' -LogGroupName 'MyLogGroup' -LogStreamName 'MyLogStream' -AuthorizationHeader 'AWS4-HMAC-SHA256 ...'
```

Configures AWS CloudWatch logging with specified log group, log stream, and AWS authorization details.

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

### -AuthorizationHeader
The AWS authorization header, generated using AWS Signature Version 4.

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

### -BaseUrl
The base URL for the AWS CloudWatch Logs API, typically \`https://logs.\<region\>.amazonaws.com\`.

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

### -LogGroupName
The name of the AWS CloudWatch Log Group to send logs to.

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

### -LogStreamName
The name of the AWS CloudWatch Log Stream within the log group.

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

### -Region
The AWS region where the CloudWatch Log Group resides, such as \`us-east-1\`.

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
This function sends logs to AWS CloudWatch in batches, using a \`ConcurrentQueue\` to manage queued logs.

## RELATED LINKS
