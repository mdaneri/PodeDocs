---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Runspaces
schema: 2.0.0
---

# Set-PodeCurrentRunspaceName

## SYNOPSIS
Sets the name of the current runspace.

## SYNTAX

```
Set-PodeCurrentRunspaceName [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The Set-PodeCurrentRunspaceName function assigns a specified name to the current runspace.
This can be useful for identifying and managing the runspace in scripts and during debugging.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeCurrentRunspaceName -Name "MyRunspace"
This command sets the name of the current runspace to "Pode_MyRunspace".
```

## PARAMETERS

### -Name
The name to assign to the current runspace.
This parameter is mandatory.

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
This is an internal function and may change in future releases of Pode.

## RELATED LINKS
