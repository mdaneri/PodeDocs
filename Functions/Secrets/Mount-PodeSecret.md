---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Mount-PodeSecret

## SYNOPSIS
Mount a Secret from a Secret Vault.

## SYNTAX

```
Mount-PodeSecret [-Name] <String> [-Vault] <String> [[-Property] <String[]>] [[-ExpandProperty] <String>]
 [-Key] <String> [[-ArgumentList] <Object[]>] [[-CacheTtl] <Int32>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Mount a Secret from a Secret Vault, so it can be more easily referenced and support caching.

## EXAMPLES

### EXAMPLE 1
```
Mount-PodeSecret -Name 'SecretName' -Vault 'VaultName' -Key 'path/to/secret' -ExpandProperty 'foo'
```

### EXAMPLE 2
```
Mount-PodeSecret -Name 'SecretName' -Vault 'VaultName' -Key 'key_of_secret' -CacheTtl 5
```

## PARAMETERS

### -ArgumentList
An optional array of Arguments to be supplied to a custom Secret Vault's scriptblocks.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CacheTtl
An optional number of minutes to Cache the Secret's value for.
You can use this parameter to override the Secret Vault's value.
(Default: -1)
If the value is -1 it uses the Secret Vault's CacheTtl.
A value of 0 is to disable caching for this Secret.
A value \>0 overrides the Secret Vault.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpandProperty
An optional Property to be expanded from the Secret and return if it contains multiple properties.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A unique friendly Name for the Secret.

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

### -Property
An optional array of Properties to be returned if the Secret contains multiple properties.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
