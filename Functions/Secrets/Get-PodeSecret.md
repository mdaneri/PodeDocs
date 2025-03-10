---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Get-PodeSecret

## SYNOPSIS
Retrieve the value of a mounted Secret.

## SYNTAX

```
Get-PodeSecret [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Retrieve the value of a mounted Secret from a Secret Vault.
You can also use "$value = $secret:\<NAME\>" syntax in certain places.

## EXAMPLES

### EXAMPLE 1
```
$value = Get-PodeSecret -Name 'SecretName'
```

### EXAMPLE 2
```
$value = $secret:SecretName
```

## PARAMETERS

### -Name
The friendly Name of a Secret.

```yaml
Type: String
Parameter Sets: (All)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
