---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# New-PodeLoggingMethod

## SYNOPSIS
Creates a new method for outputting logs (Deprecated).

## SYNTAX

### Terminal (Default)
```
New-PodeLoggingMethod [-Terminal] [-Batch <Int32>] [-BatchTimeout <Int32>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### File
```
New-PodeLoggingMethod [-File] [-Path <String>] -Name <String> [-Batch <Int32>] [-BatchTimeout <Int32>]
 [-MaxDays <Int32>] [-MaxSize <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### EventViewer
```
New-PodeLoggingMethod [-EventViewer] [-EventLogName <String>] [-Source <String>] [-EventID <Int32>]
 [-Batch <Int32>] [-BatchTimeout <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Custom
```
New-PodeLoggingMethod [-Batch <Int32>] [-BatchTimeout <Int32>] [-Custom] -ScriptBlock <ScriptBlock>
 [-ArgumentList <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function has been deprecated and will be removed in future versions.
It creates various logging methods such as Terminal, File, Event Viewer, and Custom logging.
Please use the appropriate new functions for each logging method:
- \`New-PodeTerminalLoggingMethod\` for terminal logging.
- \`New-PodeFileLoggingMethod\` for file logging.
- \`New-PodeEventViewerLoggingMethod\` for Event Viewer logging.
- \`New-PodeCustomLoggingMethod\` for custom logging.

## EXAMPLES

### EXAMPLE 1
```
$term_logging = New-PodeLoggingMethod -Terminal
```

### EXAMPLE 2
```
$file_logging = New-PodeLoggingMethod -File -Path ./logs -Name 'requests'
```

### EXAMPLE 3
```
$custom_logging = New-PodeLoggingMethod -Custom -ScriptBlock { /* logic */ }
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Custom Logging output method's ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: Custom
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Batch
An optional batch size to write log items in bulk (Default: 1)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -BatchTimeout
An optional batch timeout, in seconds, to send items off for writing if a log item isn't received (Default: 0)

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

### -Custom
If supplied, will allow you to create a Custom Logging output method.

```yaml
Type: SwitchParameter
Parameter Sets: Custom
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventID
Optional EventID for the Event Viewer (Default: 0)

```yaml
Type: Int32
Parameter Sets: EventViewer
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventLogName
Optional Log Name for the Event Viewer (Default: Application)

```yaml
Type: String
Parameter Sets: EventViewer
Aliases:

Required: False
Position: Named
Default value: Application
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventViewer
Deprecated.
Please use \`New-PodeEventViewerLoggingMethod\` instead.
If supplied, will use the inbuilt Event Viewer logging output method.

```yaml
Type: SwitchParameter
Parameter Sets: EventViewer
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -File
Deprecated.
Please use \`New-PodeFileLoggingMethod\` instead.
If supplied, will use the inbuilt File logging output method.

```yaml
Type: SwitchParameter
Parameter Sets: File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxDays
The maximum number of days to keep logs, before Pode automatically removes them.

```yaml
Type: Int32
Parameter Sets: File
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSize
The maximum size of a log file, before Pode starts writing to a new log file.

```yaml
Type: Int32
Parameter Sets: File
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The File Name to prepend new log files using.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The File Path of where to store the logs.

```yaml
Type: String
Parameter Sets: File
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

### -ScriptBlock
The ScriptBlock that defines how to output a log item.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source
Optional Source for the Event Viewer (Default: Pode)

```yaml
Type: String
Parameter Sets: EventViewer
Aliases:

Required: False
Position: Named
Default value: Pode
Accept pipeline input: False
Accept wildcard characters: False
```

### -Terminal
Deprecated.
Please use \`New-PodeTerminalLoggingMethod\` instead.
If supplied, will use the inbuilt Terminal logging output method.

```yaml
Type: SwitchParameter
Parameter Sets: Terminal
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

## RELATED LINKS
