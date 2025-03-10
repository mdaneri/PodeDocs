---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: WebSockets
schema: 2.0.0
---

# Send-PodeWebSocket

## SYNOPSIS
Send a message back to a WebSocket connection.

## SYNTAX

```
Send-PodeWebSocket [[-Name] <String>] [[-Message] <Object>] [[-Depth] <Int32>] [[-Type] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Send a message back to a WebSocket connection.

## EXAMPLES

### EXAMPLE 1
```
Send-PodeWebSocket -Name 'Example' -Message @{ message = 'Hello, there' }
```

## PARAMETERS

### -Depth
An optional Depth to parse any JSON or XML messages.
(default: 10)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### -Message
The Message to send.
Can either be a raw string, hashtable, or psobject.
Non-strings will be parsed to JSON, or the WebSocket's ContentType.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the WebSocket connection (optional if in the scope where $WsEvent is available).

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

### -Type
An optional message Type.
(default: Text)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: Text
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
