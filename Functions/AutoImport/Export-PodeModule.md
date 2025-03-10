---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: AutoImport
schema: 2.0.0
---

# Export-PodeModule

## SYNOPSIS
Exports modules that can be auto-imported by Pode, and into its runspaces.

## SYNTAX

```
Export-PodeModule [-Name] <String[]> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Exports modules that can be auto-imported by Pode, and into its runspaces.

## EXAMPLES

### EXAMPLE 1
```
Export-PodeModule -Name Mod1, Mod2
```

## PARAMETERS

### -Name
The Name(s) of modules to export.

```yaml
Type: String[]
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
