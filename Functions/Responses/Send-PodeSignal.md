---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Send-PodeSignal

## SYNOPSIS
Broadcasts a message to connected WebSocket clients.

## SYNTAX

```
Send-PodeSignal [[-Value] <Object>] [-Path <String>] [-ClientId <String>] [-Depth <Int32>] [-Mode <String>]
 [-IgnoreEvent] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Broadcasts a message to all, or some, connected WebSocket clients.
You can specify a path to send messages to, or a specific ClientId.

## EXAMPLES

### EXAMPLE 1
```
Send-PodeSignal -Value @{ Message = 'Hello, world!' }
```

### EXAMPLE 2
```
Send-PodeSignal -Value @{ Data = @(123, 100, 101) } -Path '/response-charts'
```

## PARAMETERS

### -ClientId
A specific ClientId of a connected client to send a message.
Not currently used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Depth
The Depth to generate the JSON document - the larger this value the worse performance gets.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreEvent
If supplied, if a SignalEvent is available it's data, such as path/clientId, will be ignored.

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

### -Mode
The Mode to broadcast a message: Auto, Broadcast, Direct.
(Default: Auto)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The Path of connected clients to send the message.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

### -Value
A String, PSObject, or HashTable value.
For non-string values, they will be converted to JSON.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
