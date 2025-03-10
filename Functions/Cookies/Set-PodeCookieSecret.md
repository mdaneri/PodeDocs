---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Cookies
schema: 2.0.0
---

# Set-PodeCookieSecret

## SYNOPSIS
Stores secrets that can be used to sign cookies.

## SYNTAX

### General
```
Set-PodeCookieSecret -Name <String> -Value <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Global
```
Set-PodeCookieSecret -Value <String> [-Global] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Stores secrets that can be used to sign cookies.
A global secret can be set for easier retrieval.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeCookieSecret -Name 'my-secret' -Value 'shhhh!'
```

### EXAMPLE 2
```
Set-PodeCookieSecret -Value 'hunter2' -Global
```

## PARAMETERS

### -Global
If flagged, the secret being stored will be set as the global secret.

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
The name of the secret to store.

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

### -Value
The value of the secret to store.

```yaml
Type: String
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

## NOTES

## RELATED LINKS
