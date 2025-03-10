---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: WebSockets
schema: 2.0.0
---

# Reset-PodeWebSocket

## SYNOPSIS
Reset an existing WebSocket connection.

## SYNTAX

```
Reset-PodeWebSocket [[-Name] <String>] [[-Url] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Reset an existing WebSocket connection, either using it's current URL or a new one.

## EXAMPLES

### EXAMPLE 1
```
Reset-PodeWebSocket -Name 'Example'
```

### EXAMPLE 2
```
Reset-PodeWebSocket -Name 'Example' -Url 'ws://example.com/some/socket'
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

### -Url
An optional new URL to reset the connection to.
If not supplied, the connection's original URL will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
