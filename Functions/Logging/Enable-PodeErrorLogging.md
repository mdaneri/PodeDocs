---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Enable-PodeErrorLogging

## SYNOPSIS
Enables Error Logging using a supplied output method.

## SYNTAX

```
Enable-PodeErrorLogging [-Method] <Hashtable[]> [[-Levels] <String[]>] [-Raw] [-DisableDefaultLog]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Enables Error Logging using a supplied output method.

## EXAMPLES

### EXAMPLE 1
```
New-PodeLoggingMethod -Terminal | Enable-PodeErrorLogging
```

## PARAMETERS

### -DisableDefaultLog
If supplied, the error logs will NOT be duplicated to the default logging method.

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

### -Levels
The Levels of errors that should be logged (default is Error).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: @('Error')
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
The Method to use for output the log entry (From New-PodeLoggingMethod).

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
If supplied, the log item returned will be the raw Error item as a hashtable and not a string (for Custom methods).

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
