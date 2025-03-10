---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Get-PodeLoggerLevel

## SYNOPSIS
Retrieves the logging levels for a specified logger or predefined log type in Pode.

## SYNTAX

### ByName
```
Get-PodeLoggerLevel [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ByType
```
Get-PodeLoggerLevel [-Type] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function retrieves the logging levels configured for a specified Pode logger.
It supports both predefined log types ('Error', 'Default', 'Request') and custom logger names.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeLoggerLevel -Type Error
# Retrieves the logging levels for error logging.
```

### EXAMPLE 2
```
Get-PodeLoggerLevel -Type Default
# Retrieves the logging levels for default logging.
```

### EXAMPLE 3
```
Get-PodeLoggerLevel -Type Request
# Retrieves the logging levels for request logging.
```

### EXAMPLE 4
```
Get-PodeLoggerLevel -Name 'MyCustomLogger'
# Retrieves the logging levels for a custom logger named 'MyCustomLogger'.
```

## PARAMETERS

### -Name
The name of the logger to retrieve.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
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

### -Type
The type of predefined logging to retrieve levels for.
Accepted values: 'Error', 'Default', 'Request'.

```yaml
Type: String
Parameter Sets: ByType
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### An array of logging levels.
## NOTES

## RELATED LINKS
