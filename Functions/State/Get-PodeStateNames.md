---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: State
schema: 2.0.0
---

# Get-PodeStateNames

## SYNOPSIS
Returns the current names of state variables.

## SYNTAX

```
Get-PodeStateNames [[-Pattern] <String>] [[-Scope] <String[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Returns the current names of state variables that have been set.
You can filter the result using Scope or a Pattern.

## EXAMPLES

### EXAMPLE 1
```
'
```

### EXAMPLE 2
```
$names = Get-PodeStateNames -Pattern '^\w+[0-9]{0,2}$'
```

## PARAMETERS

### -Pattern
An optional regex Pattern to filter the state names.

```yaml
Type: String
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

### -Scope
An optional Scope to filter the state names.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
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
