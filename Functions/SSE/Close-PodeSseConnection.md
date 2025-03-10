---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Close-PodeSseConnection

## SYNOPSIS
Close one or more SSE connections.

## SYNTAX

```
Close-PodeSseConnection [-Name] <String> [[-Group] <String[]>] [[-ClientId] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Close one or more SSE connections.
Either all connections for an SSE connection Name, or specific ClientIds for a Name.

## EXAMPLES

### EXAMPLE 1
```
Close-PodeSseConnection -Name 'Actions'
```

### EXAMPLE 2
```
Close-PodeSseConnection -Name 'Actions' -Group 'admins'
```

### EXAMPLE 3
```
Close-PodeSseConnection -Name 'Actions' -ClientId @('my-client-id', 'my-other'id')
```

## PARAMETERS

### -ClientId
An optional array of 1 or more SSE connection ClientIds, that are for the SSE connection Name.
If not supplied, every SSE connection for the supplied Name will be closed.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Group
An optional array of 1 or more SSE connection Groups, that are for the SSE connection Name.
If supplied without any ClientIds, then all connections for the Group(s) will be closed.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the SSE connection which has the ClientIds for the connections to close.
If supplied on its own, all connections will be closed.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
