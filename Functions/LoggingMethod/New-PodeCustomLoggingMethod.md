---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: LoggingMethod
schema: 2.0.0
---

# New-PodeCustomLoggingMethod

## SYNOPSIS
Creates a new custom logging method in Pode.

## SYNTAX

### DataFormat (Default)
```
New-PodeCustomLoggingMethod -ScriptBlock <ScriptBlock> [-ArgumentList <Object[]>] [-CustomOptions <Hashtable>]
 [-FailureAction <String>] [-DataFormat <String>] [-AsUTC] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### ISO8601
```
New-PodeCustomLoggingMethod -ScriptBlock <ScriptBlock> [-ArgumentList <Object[]>] [-CustomOptions <Hashtable>]
 [-FailureAction <String>] [-ISO8601] [-AsUTC] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function sets up a custom logging method that uses a script block to define the logging logic.
It supports the option to run the logging method in a separate runspace and allows for custom options, date formatting, and failure handling.

## EXAMPLES

### EXAMPLE 1
```
$logMethod = New-PodeCustomLoggingMethod -ScriptBlock { param($logItem) Write-Output $logItem } -UseRunspace
```

Creates a custom logging method using a script block that writes log items to the output.
The method runs in a separate runspace.

### EXAMPLE 2
```
$logMethod = New-PodeCustomLoggingMethod -ScriptBlock { param($logItem) Write-Output $logItem } -DataFormat 'yyyy/MM/dd HH:mm:ss'
```

Creates a custom logging method with a custom date format.

## PARAMETERS

### -ArgumentList
An array of arguments to pass to the custom script block.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -CustomOptions
A hashtable of custom options that will be passed to the script block when used inside a runspace.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: @{}
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

### -ScriptBlock
A non-empty script block that defines the custom logging logic.
This parameter is mandatory.

```yaml
Type: ScriptBlock
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

### Hashtable: Returns a hashtable containing the custom logging method configuration.
## NOTES

## RELATED LINKS
