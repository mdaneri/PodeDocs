---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Metrics
schema: 2.0.0
---

# Get-PodeServerUptime

## SYNOPSIS
Retrieves the server uptime in milliseconds or a human-readable format.

## SYNTAX

```
Get-PodeServerUptime [-Total] [[-Format] <String>] [-ExcludeMilliseconds] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
The \`Get-PodeServerUptime\` function calculates the server's uptime since its last start or total uptime since initial load, depending on the \`-Total\` switch.
By default, the uptime is returned in milliseconds.
When the \`-Format\` parameter is used, the uptime can be returned in various human-readable styles:
- \`Milliseconds\` (default): Raw uptime in milliseconds.
- \`Concise\`: A short format like "1d 2h 3m".
- \`Compact\`: A condensed format like "01:10:17:36".
- \`Verbose\`: A detailed format like "1 day, 2 hours, 3 minutes, 5 seconds, 200 milliseconds".
The \`-ExcludeMilliseconds\` switch allows removal of milliseconds from human-readable output.

## EXAMPLES

### EXAMPLE 1
```
$currentUptime = Get-PodeServerUptime
# Output: 123456789 (milliseconds)
```

### EXAMPLE 2
```
$totalUptime = Get-PodeServerUptime -Total
# Output: 987654321 (milliseconds)
```

### EXAMPLE 3
```
$readableUptime = Get-PodeServerUptime -Format Concise
# Output: "1d 10h 17m"
```

### EXAMPLE 4
```
$verboseUptime = Get-PodeServerUptime -Format Verbose
# Output: "1 day, 10 hours, 17 minutes, 36 seconds, 789 milliseconds"
```

### EXAMPLE 5
```
$compactUptime = Get-PodeServerUptime -Format Compact
# Output: "01:10:17:36"
```

### EXAMPLE 6
```
$compactUptimeNoMs = Get-PodeServerUptime -Format Compact -ExcludeMilliseconds
# Output: "01:10:17:36"
```

## PARAMETERS

### -ExcludeMilliseconds
Omits milliseconds from the human-readable output when \`-Format\` is not \`Milliseconds\`.

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

### -Format
Specifies the desired output format for the uptime.
Allowed values:
- \`Milliseconds\` (default): Uptime in raw milliseconds.
- \`Concise\`: Human-readable in a short form (e.g., "1d 2h 3m").
- \`Compact\`: Condensed form (e.g., "01:10:17:36").
- \`Verbose\`: Detailed format (e.g., "1 day, 2 hours, 3 minutes, 5 seconds").

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: Milliseconds
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

### -Total
Retrieves the total server uptime since the initial load, regardless of any restarts.

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

### System.Int64
### System.String
## NOTES
This function is part of Pode's utility metrics to monitor server uptime.

## RELATED LINKS
