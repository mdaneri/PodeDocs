---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Test-PodeSecretVault

## SYNOPSIS
Tests if a Secret Vault has been registered.

## SYNTAX

```
Test-PodeSecretVault [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Tests if a Secret Vault has been registered.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeSecretVault -Name 'VaultName') { ... }
```

## PARAMETERS

### -Name
The Name of the Secret Vault to test.

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
