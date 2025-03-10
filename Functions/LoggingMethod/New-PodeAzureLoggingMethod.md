---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeAzureLoggingMethod

## SYNOPSIS
Configures logging to Azure Monitor Logs.

## SYNTAX

### DataFormat
```
New-PodeAzureLoggingMethod -WorkspaceId <String> -AuthorizationHeader <String> [-LogType <String>]
 [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC] [-DefaultTag <String>] [-DataFormat <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ISO8601
```
New-PodeAzureLoggingMethod -WorkspaceId <String> -AuthorizationHeader <String> [-LogType <String>]
 [-FailureAction <String>] [-SkipCertificateCheck] [-AsUTC] [-DefaultTag <String>] [-ISO8601]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`New-PodeAzureLoggingMethod\` function sets up logging for Azure Monitor Logs, allowing log data to be sent to a specified Azure Log Analytics workspace.
It uses the shared key authorization method to authenticate with Azure.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAzureLoggingMethod -WorkspaceId '12345' -AuthorizationHeader 'SharedKey 12345:abcdef...' -LogType 'ApplicationLogs'
```

Sets up Azure Monitor logging with the specified workspace ID and authorization details.

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
The authorization header for Azure, generated using the Workspace ID and shared key.

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

### -LogType
The custom log type name in Azure Monitor.
Defaults to \`CustomLog\`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: CustomLog
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

### -WorkspaceId
The Azure Log Analytics Workspace ID.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable
## NOTES
This function sends logs to Azure Monitor Logs using the Azure REST API, formatted for ingestion by Azure Log Analytics.

## RELATED LINKS
