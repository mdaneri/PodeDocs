---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: EndWare
schema: 2.0.0
---

# Use-PodeEndware

## SYNOPSIS
Automatically loads endware ps1 files

## SYNTAX

```
Use-PodeEndware [[-Path] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Automatically loads endware ps1 files from either a /endware folder, or a custom folder.
Saves space dot-sourcing them all one-by-one.

## EXAMPLES

### EXAMPLE 1
```
Use-PodeEndware
```

### EXAMPLE 2
```
Use-PodeEndware -Path './endware'
```

## PARAMETERS

### -Path
Optional Path to a folder containing ps1 files, can be relative or literal.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
