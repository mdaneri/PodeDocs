---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Read-PodeSecret

## SYNOPSIS
Read a Secret from a Secret Vault.

## SYNTAX

```
Read-PodeSecret [-Key] <String> [-Vault] <String> [[-Property] <String[]>] [[-ExpandProperty] <String>]
 [[-ArgumentList] <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Read a Secret from a Secret Vault.

## EXAMPLES

### EXAMPLE 1
```
$value = Read-PodeSecret -Key 'path/to/secret' -Vault 'VaultName'
```

### EXAMPLE 2
```
$value = Read-PodeSecret -Key 'key_of_secret' -Vault 'VaultName' -Property prop1, prop2
```

## PARAMETERS

### -ArgumentList
An optional array of Arguments to be supplied to a custom Secret Vault's scriptblocks.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
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
