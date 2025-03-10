---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Set-PodeSseBroadcastLevel

## SYNOPSIS
Set an allowed broadcast level for SSE connections.

## SYNTAX

```
Set-PodeSseBroadcastLevel [[-Name] <String>] [[-Type] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Set an allowed broadcast level for SSE connections, either for all SSE connection names or specific ones.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSseBroadcastLevel -Type Name
```

### EXAMPLE 2
```
Set-PodeSseBroadcastLevel -Type Group
```

### EXAMPLE 3
```
Set-PodeSseBroadcastLevel -Name 'Actions' -Type ClientId
```

## PARAMETERS

### -Name
An optional Name for an SSE connection (default: *).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: *
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
The broadcast level Type for the SSE connection.
Name = Allow broadcasting at all levels, including broadcasting to all Groups and/or ClientIds for an SSE connection Name.
Group = Allow broadcasting to only Groups or specific ClientIds.
If neither Groups nor ClientIds are supplied, sending an event will fail.
ClientId = Allow broadcasting to only ClientIds.
If no ClientIds are supplied, sending an event will fail.

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
