---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: WebSockets
schema: 2.0.0
---

# Connect-PodeWebSocket

## SYNOPSIS
Connect to an external WebSocket.

## SYNTAX

### Script (Default)
```
Connect-PodeWebSocket -Name <String> -Url <String> [-ScriptBlock <ScriptBlock>] [-ContentType <String>]
 [-ArgumentList <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Connect-PodeWebSocket -Name <String> -Url <String> -FilePath <String> [-ContentType <String>]
 [-ArgumentList <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Connect to an external WebSocket.

## EXAMPLES

### EXAMPLE 1
```
Connect-PodeWebSocket -Name 'Example' -Url 'ws://example.com/some/socket' -ScriptBlock { ... }
```

### EXAMPLE 2
```
Connect-PodeWebSocket -Name 'Example' -Url 'ws://example.com/some/socket' -ScriptBlock { param($arg1, $arg2) ... } -ArgumentList 'arg1', 'arg2'
```

### EXAMPLE 3
```
Connect-PodeWebSocket -Name 'Example' -Url 'ws://example.com/some/socket' -FilePath './some/path/file.ps1'
```

### EXAMPLE 4
```
Connect-PodeWebSocket -Name 'Example' -Url 'ws://example.com/some/socket' -ScriptBlock { ... } -ContentType 'text/xml'
```

## PARAMETERS

### -ArgumentList
AN optional array of extra arguments, that will be passed to the ScriptBlock.

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

### -ContentType
An optional ContentType for parsing/converting received/sent messages.
(default: application/json)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Application/json
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the WebSocket's logic.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the WebSocket connection.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -ScriptBlock
The ScriptBlock to invoke for processing received messages from the WebSocket.
The ScriptBlock will have access to a $WsEvent variable with details of the received message.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url
The URL of the WebSocket.
Should start with either ws:// or wss://.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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
