---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Close-PodeDisposable

## SYNOPSIS
Dispose and close streams, tokens, and other Disposables.

## SYNTAX

```
Close-PodeDisposable [[-Disposable] <IDisposable>] [-Close] [-CheckNetwork]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Dispose and close streams, tokens, and other Disposables.

## EXAMPLES

### EXAMPLE 1
```
Close-PodeDisposable -Disposable $stream -Close
```

## PARAMETERS

### -CheckNetwork
If an error is thrown, check the reason - if it's network related ignore the error.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Close
Should the Disposable also be closed, as well as disposed?

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disposable
The Disposable object to dispose and close.

```yaml
Type: IDisposable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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
