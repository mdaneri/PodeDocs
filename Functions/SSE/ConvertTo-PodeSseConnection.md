---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# ConvertTo-PodeSseConnection

## SYNOPSIS
Converts the current HTTP request to a Route to be an SSE connection.

## SYNTAX

```
ConvertTo-PodeSseConnection [-Name] <String> [[-Group] <String>] [[-Scope] <String>] [[-RetryDuration] <Int32>]
 [[-ClientId] <String>] [-AllowAllOrigins] [-Force] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Converts the current HTTP request to a Route to be an SSE connection, by sending the required headers back to the client.
The connection can only be configured if the request's Accept header is "text/event-stream", unless Forced.

## EXAMPLES

### EXAMPLE 1
```
ConvertTo-PodeSseConnection -Name 'Actions'
```

### EXAMPLE 2
```
ConvertTo-PodeSseConnection -Name 'Actions' -Scope Local
```

### EXAMPLE 3
```
ConvertTo-PodeSseConnection -Name 'Actions' -Group 'admins'
```

### EXAMPLE 4
```
ConvertTo-PodeSseConnection -Name 'Actions' -AllowAllOrigins
```

### EXAMPLE 5
```
ConvertTo-PodeSseConnection -Name 'Actions' -ClientId 'my-client-id'
```

## PARAMETERS

### -AllowAllOrigins
If supplied, then Access-Control-Allow-Origin will be set to * on the response.

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

### -ClientId
An optional ClientId to use for the SSE connection, this value will be signed if signing is enabled (Default: GUID).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
If supplied, the Accept header of the request will be ignored; attempting to configure an SSE connection even if the header isn't "text/event-stream".

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

### -Group
An optional Group for this SSE connection, to enable broadcasting events to all connections for an SSE connection name in a Group.

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

### -Name
The Name of the SSE connection, which ClientIds will be stored under.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -RetryDuration
An optional RetryDuration, in milliseconds, for the period of time a browser should wait before reattempting a connection if lost (Default: 0).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
The Scope of the SSE connection, either Default, Local or Global (Default: Default).
- If the Scope is Default, then it will be Global unless the default has been updated via Set-PodeSseDefaultScope.
- If the Scope is Local, then the SSE connection will only be opened for the duration of the request to a Route that configured it.
- If the Scope is Global, then the SSE connection will be cached internally so events can be sent to the connection from Tasks, Timers, and other Routes, etc.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
