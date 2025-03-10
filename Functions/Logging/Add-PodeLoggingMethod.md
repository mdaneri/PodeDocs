---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Add-PodeLoggingMethod

## SYNOPSIS
Enables a generic logging method in Pode.

## SYNTAX

```
Add-PodeLoggingMethod [-Method] <Hashtable[]> [-Name] <String> [[-Levels] <String[]>] [-Raw]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function enables a generic logging method in Pode, allowing logs to be written based on the defined method and log levels.
It ensures the method is not already enabled and validates the provided script block.

## EXAMPLES

### EXAMPLE 1
```
$method = New-PodeLoggingMethod -syslog -Server 127.0.0.1 -Transport UDP
$method | Add-PodeLoggingMethod -Name "mysyslog"
```

## PARAMETERS

### -Levels
An array of log levels to be enabled for the logging method (Default: 'Error', 'Emergency', 'Alert', 'Critical', 'Warning', 'Notice', 'Informational', 'Info', 'Verbose', 'Debug').

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: @('Error', 'Emergency', 'Alert', 'Critical', 'Warning', 'Notice', 'Informational')
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
The hashtable defining the logging method, including the ScriptBlock for log output.

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
The name of the logging method to be enabled.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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

### -Raw
If set, the raw log data will be included in the logging output.

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

## NOTES

## RELATED LINKS
