---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Set-PodeSecret

## SYNOPSIS
Create/update a Secret in a Secret Vault.

## SYNTAX

```
Set-PodeSecret -Key <String> -Vault <String> [-InputObject] <Object> [-Metadata <Hashtable>]
 [-ArgumentList <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Create/update a Secret in a Secret Vault.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSecret -Key 'path/to/secret' -Vault 'VaultName' -InputObject 'value'
```

### EXAMPLE 2
```
Set-PodeSecret -Key 'key_of_secret' -Vault 'VaultName' -InputObject @{ key = value }
```

## PARAMETERS

### -ArgumentList
An optional array of Arguments to be supplied to a custom Secret Vault's scriptblocks.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
The value to use when updating the Secret.
Only the following object types are supported: byte\[\], string, securestring, pscredential, hashtable.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Key
The Key/Path of the Secret within the Secret Vault.

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

### -Metadata
An optional Metadata hashtable.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
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

### -Vault
The friendly name of the Secret Vault this Secret should be created in.

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
