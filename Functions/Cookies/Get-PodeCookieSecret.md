---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Cookies
schema: 2.0.0
---

# Get-PodeCookieSecret

## SYNOPSIS
Retrieves a stored secret value.

## SYNTAX

### General
```
Get-PodeCookieSecret -Name <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Global
```
Get-PodeCookieSecret [-Global] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Retrieves a stored secret value.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeCookieSecret -Name 'my-secret'
```

### EXAMPLE 2
```
Get-PodeCookieSecret -Global
```

## PARAMETERS

### -Global
If flagged, will return the current global secret value.

```yaml
Type: SwitchParameter
Parameter Sets: Global
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the secret to retrieve.

```yaml
Type: String
Parameter Sets: General
Aliases:

Required: True
Position: Named
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.String
## NOTES

## RELATED LINKS
