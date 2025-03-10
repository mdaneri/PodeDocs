---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Timers
schema: 2.0.0
---

# Invoke-PodeTimer

## SYNOPSIS
Adhoc invoke a Timer's logic.

## SYNTAX

```
Invoke-PodeTimer [-Name] <String> [-ArgumentList <Object[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Adhoc invoke a Timer's logic outside of its defined interval.
This invocation doesn't count towards the Timer's limit.

## EXAMPLES

### EXAMPLE 1
```
Invoke-PodeTimer -Name 'timer-name'
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Timer's ScriptBlock.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
