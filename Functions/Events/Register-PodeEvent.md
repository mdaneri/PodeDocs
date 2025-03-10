---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Events
schema: 2.0.0
---

# Register-PodeEvent

## SYNOPSIS
Registers a script to be run when a certain server event occurs within Pode

## SYNTAX

```
Register-PodeEvent [-Type] <PodeServerEventType> [-Name] <String> [-ScriptBlock] <ScriptBlock>
 [[-ArgumentList] <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Registers a script to be run when a certain server event occurs within Pode, such as Start, Terminate, and Restart.

## EXAMPLES

### EXAMPLE 1
```
Register-PodeEvent -Type Start -Name 'Event1' -ScriptBlock { }
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A unique Name for the registered event.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
A ScriptBlock to invoke when the event is triggered.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Type
The Type of event to be registered.

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
