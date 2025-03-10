---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Handlers
schema: 2.0.0
---

# Add-PodeHandler

## SYNOPSIS
Adds a Handler of a specific Type.

## SYNTAX

### Script (Default)
```
Add-PodeHandler -Type <String> -Name <String> -ScriptBlock <ScriptBlock> [-ArgumentList <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodeHandler -Type <String> -Name <String> -FilePath <String> [-ArgumentList <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a Handler of a specific Type.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeHandler -Type Smtp -Name 'Main' -ScriptBlock { /* logic */ }
```

### EXAMPLE 2
```
Add-PodeHandler -Type Service -Name 'Looper' -ScriptBlock { /* logic */ }
```

### EXAMPLE 3
```
Add-PodeHandler -Type Smtp -Name 'Main' -ScriptBlock { /* logic */ } -ArgumentList 'arg1', 'arg2'
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Handler's ScriptBlock.

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

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the Handler's main logic.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Handler.

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

### -ScriptBlock
The ScriptBlock for the Handler's main logic.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
The Type of the Handler.

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
