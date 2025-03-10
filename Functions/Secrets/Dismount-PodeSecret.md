---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Dismount-PodeSecret

## SYNOPSIS
Dismount a previously mounted Secret.

## SYNTAX

```
Dismount-PodeSecret [-Name] <String> [-Remove] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Dismount a previously mounted Secret.

## EXAMPLES

### EXAMPLE 1
```
Dismount-PodeSecret -Name 'SecretName'
```

### EXAMPLE 2
```
Dismount-PodeSecret -Name 'SecretName' -Remove
```

## PARAMETERS

### -Name
The friendly Name of the Secret.

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

### -Remove
If supplied, the Secret will also be removed from the Secret Vault as well.

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
