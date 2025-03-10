---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# Get-PodeAccess

## SYNOPSIS
Get one or more Access methods.

## SYNTAX

```
Get-PodeAccess [[-Name] <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Get one or more Access methods.

## EXAMPLES

### EXAMPLE 1
```
$methods = Get-PodeAccess
```

### EXAMPLE 2
```
$methods = Get-PodeAccess -Name 'Example'
```

### EXAMPLE 3
```
$methods = Get-PodeAccess -Name 'Example1', 'Example2'
```

## PARAMETERS

### -Name
The Name of the Access method.
If no name supplied, all methods will be returned.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
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

### System.Object[]
## NOTES

## RELATED LINKS
