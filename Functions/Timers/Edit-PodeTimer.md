---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Timers
schema: 2.0.0
---

# Edit-PodeTimer

## SYNOPSIS
Edits an existing Timer.

## SYNTAX

```
Edit-PodeTimer [-Name] <String> [-Interval <Int32>] [-ScriptBlock <ScriptBlock>] [-ArgumentList <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Edits an existing Timer's properties, such as interval or scriptblock.

## EXAMPLES

### EXAMPLE 1
```
Edit-PodeTimer -Name 'Hello' -Interval 10
```

## PARAMETERS

### -ArgumentList
Any new Arguments for the Timer.

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

### -Interval
The new Interval for the Timer in seconds.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Timer.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -ScriptBlock
The new ScriptBlock for the Timer.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

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
