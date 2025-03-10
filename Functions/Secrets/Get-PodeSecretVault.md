---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Get-PodeSecretVault

## SYNOPSIS
Fetches and returns information of a Secret Vault.

## SYNTAX

```
Get-PodeSecretVault [-Name] <String[]> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Fetches and returns information of a Secret Vault.

## EXAMPLES

### EXAMPLE 1
```
$vault = Get-PodeSecretVault -Name 'VaultName'
```

### EXAMPLE 2
```
$vaults = Get-PodeSecretVault -Name 'VaultName1', 'VaultName2'
```

## PARAMETERS

### -Name
The Name(s) of a Secret Vault to retrieve.

```yaml
Type: String[]
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
