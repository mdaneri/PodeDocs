---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Events
schema: 2.0.0
---

# Unregister-PodeEvent

## SYNOPSIS
Unregisters an event that has been registered with the specified Name.

## SYNTAX

```
Unregister-PodeEvent [-Type] <PodeServerEventType> [-Name] <String> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Unregisters an event that has been registered with the specified Name.

## EXAMPLES

### EXAMPLE 1
```
Unregister-PodeEvent -Type Start -Name 'Event1'
```

## PARAMETERS

### -Name
The Name of the event to unregister.

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

### -Type
The Type of the event to unregister.

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
