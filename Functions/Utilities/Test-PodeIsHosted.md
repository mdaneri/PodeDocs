---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Test-PodeIsHosted

## SYNOPSIS
Returns whether or not the server is being hosted behind another application.

## SYNTAX

```
Test-PodeIsHosted [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns whether or not the server is being hosted behind another application, such as Heroku or IIS.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeIsHosted) { }
```

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
