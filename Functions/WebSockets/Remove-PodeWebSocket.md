---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: WebSockets
schema: 2.0.0
---

# Remove-PodeWebSocket

## SYNOPSIS
Remove a WebSocket connection.

## SYNTAX

```
Remove-PodeWebSocket [[-Name] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Disconnects and then removes a WebSocket connection.

## EXAMPLES

### EXAMPLE 1
```
Remove-PodeWebSocket -Name 'Example'
```

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
