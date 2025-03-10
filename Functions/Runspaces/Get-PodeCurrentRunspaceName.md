---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Runspaces
schema: 2.0.0
---

# Get-PodeCurrentRunspaceName

## SYNOPSIS
Retrieves the name of the current PowerShell runspace.

## SYNTAX

```
Get-PodeCurrentRunspaceName [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The Get-PodeCurrentRunspaceName function retrieves the name of the current PowerShell runspace.
This can be useful for debugging or logging purposes to identify the runspace in use.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeCurrentRunspaceName
Returns the name of the current runspace.
```

## PARAMETERS

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
