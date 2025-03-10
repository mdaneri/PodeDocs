---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Enable-PodeRequestLogging

## SYNOPSIS
Enables Request Logging using a supplied output method.

## SYNTAX

```
Enable-PodeRequestLogging [-Method] <Hashtable[]> [[-UsernameProperty] <String>] [-Raw] [[-LogFormat] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Enables Request Logging using a supplied output method.

## EXAMPLES

### EXAMPLE 1
```
New-PodeLoggingMethod -Terminal | Enable-PodeRequestLogging
```

## PARAMETERS

### -LogFormat
The format to use for the log entries.
Options are: Extended, Common, Combined, JSON (Default: Combined).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Combined
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
If supplied, the log item returned will be the raw Request item as a hashtable and not a string.

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

### -UsernameProperty
An optional property path within the $WebEvent.Auth.User object for the user's Username.
(Default: Username).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
