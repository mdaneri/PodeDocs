---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Test-PodeLoggerEnabled

## SYNOPSIS
Determines if a specified logger or a predefined log type is enabled.

## SYNTAX

### ByName
```
Test-PodeLoggerEnabled [[-Name] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ByType
```
Test-PodeLoggerEnabled [[-Type] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function checks if logging is enabled in Pode and verifies if the specified logger or a predefined log type
(Error, Default, Request) exists within the logging configuration.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeLoggerEnabled -Name 'MyCustomLogger'
# Checks if the custom logger 'MyCustomLogger' is enabled.
```

### EXAMPLE 2
```
Test-PodeLoggerEnabled -Type Error
# Checks if error logging is enabled.
```

### EXAMPLE 3
```
Test-PodeLoggerEnabled -Type Default
# Checks if default logging is enabled.
```

### EXAMPLE 4
```
Test-PodeLoggerEnabled -Type Request
# Checks if request logging is enabled.
```

## PARAMETERS

### -Name
The name of the logger to check.
If not specified, it checks if logging is generally enabled.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
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
The type of predefined logging to check.
Accepted values: 'Error', 'Default', 'Request'.

```yaml
Type: String
Parameter Sets: ByType
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
