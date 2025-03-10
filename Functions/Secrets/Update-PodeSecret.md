---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Update-PodeSecret

## SYNOPSIS
Update the value of a mounted Secret.

## SYNTAX

```
Update-PodeSecret -Name <String> [-InputObject] <Object> [-Metadata <Hashtable>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Update the value of a mounted Secret in a Secret Vault.
You can also use "$secret:\<NAME\> = $value" syntax in certain places.

## EXAMPLES

### EXAMPLE 1
```
Update-PodeSecret -Name 'SecretName' -InputObject @{ key = value }
```

### EXAMPLE 2
```
Update-PodeSecret -Name 'SecretName' -InputObject 'value'
```

### EXAMPLE 3
```
$secret:SecretName = 'value'
```

## PARAMETERS

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

### -Name
The friendly Name of a Secret.

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
