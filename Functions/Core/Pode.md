---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Pode

## SYNOPSIS
The CLI for Pode, to initialise, build and start your Server.

## SYNTAX

```
Pode [-Action] <String> [-Dev] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The CLI for Pode, to initialise, build and start your Server.

## EXAMPLES

### EXAMPLE 1
```
pode install -dev
```

### EXAMPLE 2
```
pode build
```

### EXAMPLE 3
```
pode start
```

## PARAMETERS

### -Action
The action to invoke on your Server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: a

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dev
Supply when running "pode install", this will install any dev packages defined in your package.json.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: d

Required: False
Position: Named
Default value: False
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
