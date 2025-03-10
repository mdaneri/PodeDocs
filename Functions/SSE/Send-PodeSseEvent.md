---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Send-PodeSseEvent

## SYNOPSIS
Send an Event to one or more SSE connections.

## SYNTAX

### WebEvent (Default)
```
Send-PodeSseEvent [-Data] <Object> [-Id <String>] [-EventType <String>] [-Depth <Int32>] [-FromEvent]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Name
```
Send-PodeSseEvent [-Data] <Object> -Name <String> [-Group <String[]>] [-ClientId <String[]>] [-Id <String>]
 [-EventType <String>] [-Depth <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Send an Event to one or more SSE connections.
This can either be:
- Every client for an SSE connection Name
- Specific ClientIds for an SSE connection Name
- The current SSE connection being referenced within $WebEvent.Sse

## EXAMPLES

### EXAMPLE 1
```
Send-PodeSseEvent -FromEvent -Data 'This is an event'
```

### EXAMPLE 2
```
Send-PodeSseEvent -FromEvent -Data @{ Message = 'A message' }
```

### EXAMPLE 3
```
Send-PodeSseEvent -Name 'Actions' -Data @{ Message = 'A message' }
```

### EXAMPLE 4
```
Send-PodeSseEvent -Name 'Actions' -Group 'admins' -Data @{ Message = 'A message' }
```

### EXAMPLE 5
```
Send-PodeSseEvent -Name 'Actions' -Data @{ Message = 'A message' } -ID 123 -EventType 'action'
```

## PARAMETERS

### -ClientId
An optional array of 1 or more SSE connection ClientIds to send Events to, for the specified SSE connection Name.

```yaml
Type: String[]
Parameter Sets: Name
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Data
The Data for the Event being sent, either as a String or a Hashtable/PSObject.
If the latter, it will be converted into JSON.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### -EventType
An optional EventType for the Event being sent.

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

### -FromEvent
If supplied, the SSE connection Name and ClientId will atttempt to be retrived from $WebEvent.Sse.
These details will be set if ConvertTo-PodeSseConnection has just been called.
Or if X-PODE-SSE-CLIENT-ID and X-PODE-SSE-NAME are set on an HTTP request.

```yaml
Type: SwitchParameter
Parameter Sets: WebEvent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Group
An optional array of 1 or more SSE connection Groups to send Events to, for the specified SSE connection Name.

```yaml
Type: String[]
Parameter Sets: Name
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
An optional ID for the Event being sent.

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

### -Name
An SSE connection Name.

```yaml
Type: String
Parameter Sets: Name
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
