---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Events
schema: 2.0.0
---

# Clear-PodeEvent

## SYNOPSIS
Clears an event of all registered scripts.

## SYNTAX

```
Clear-PodeEvent [-Type] <PodeServerEventType> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Clears an event of all registered scripts.

## EXAMPLES

### EXAMPLE 1
```
Clear-PodeEvent -Type Start
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

### -Type
The Type of event to clear.

```yaml
Type: PodeServerEventType
Parameter Sets: (All)
Aliases:
Accepted values: Start, Starting, Terminate, Restarting, Restart, Browser, Crash, Stop, Running, Suspending, Suspend, Resuming, Resume, Enable, Disable

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

## NOTES

## RELATED LINKS
