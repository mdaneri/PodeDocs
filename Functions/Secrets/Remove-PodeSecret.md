---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Remove-PodeSecret

## SYNOPSIS
Remove a Secret from a Secret Vault.

## SYNTAX

```
Remove-PodeSecret [-Key] <String> [-Vault] <String> [[-ArgumentList] <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Remove a Secret from a Secret Vault.
To remove a mounted Secret, you can pass the Remove switch to Dismount-PodeSecret.

## EXAMPLES

### EXAMPLE 1
```
Remove-PodeSecret -Key 'path/to/secret' -Vault 'VaultName'
```

## PARAMETERS

### -ArgumentList
An optional array of Arguments to be supplied to a custom Secret Vault's scriptblocks.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Key
The Key/Path of the Secret within the Secret Vault.

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

### -Vault
The friendly name of the Secret Vault this Secret can be found in.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
