---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: WebSockets
schema: 2.0.0
---

# Set-PodeWebSocketConcurrency

## SYNOPSIS
Set the maximum number of concurrent WebSocket connection threads.

## SYNTAX

```
Set-PodeWebSocketConcurrency [-Maximum] <Int32> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Set the maximum number of concurrent WebSocket connection threads.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeWebSocketConcurrency -Maximum 5
```

## PARAMETERS

### -Maximum
The Maximum number of threads available to process WebSocket connection messages received.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: 0
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
