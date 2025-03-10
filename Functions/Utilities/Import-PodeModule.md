---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Import-PodeModule

## SYNOPSIS
Imports a Module into the current, and all runspaces that Pode uses.

## SYNTAX

### Name (Default)
```
Import-PodeModule -Name <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Path
```
Import-PodeModule -Path <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Imports a Module into the current, and all runspaces that Pode uses.
Modules can also be imported from the ps_modules directory.

## EXAMPLES

### EXAMPLE 1
```
Import-PodeModule -Name IISManager
```

### EXAMPLE 2
```
Import-PodeModule -Path './modules/utilities.psm1'
```

## PARAMETERS

### -Name
The name of a globally installed Module, or one within the ps_modules directory, to import.

```yaml
Type: String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The path, literal or relative, to a Module to import.

```yaml
Type: String
Parameter Sets: Path
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
