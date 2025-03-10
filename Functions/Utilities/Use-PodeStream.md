---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Use-PodeStream

## SYNOPSIS
Like the "using" keyword in .NET.
Allows you to use a Stream and then disposes of it.

## SYNTAX

```
Use-PodeStream [-Stream] <IDisposable> [-ScriptBlock] <ScriptBlock> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Like the "using" keyword in .NET.
Allows you to use a Stream and then disposes of it.

## EXAMPLES

### EXAMPLE 1
```
$content = (Use-PodeStream -Stream $stream -ScriptBlock { return $args[0].ReadToEnd() })
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

### -ScriptBlock
The ScriptBlock to invoke.
It will be supplied the Stream.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stream
The Stream to use and then dispose.

```yaml
Type: IDisposable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
