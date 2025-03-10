---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Test-PodeSseBroadcastLevel

## SYNOPSIS
Test if an SSE connection can be broadcasted to, given the Name, Group, and ClientIds.

## SYNTAX

```
Test-PodeSseBroadcastLevel [-Name] <String> [[-Group] <String[]>] [[-ClientId] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Test if an SSE connection can be broadcasted to, given the Name, Group, and ClientIds.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeSseBroadcastLevel -Name 'Actions') { ... }
```

### EXAMPLE 2
```
if (Test-PodeSseBroadcastLevel -Name 'Actions' -Group 'admins') { ... }
```

### EXAMPLE 3
```
if (Test-PodeSseBroadcastLevel -Name 'Actions' -ClientId 'my-client-id') { ... }
```

## PARAMETERS

### -ClientId
An array of 1 or more ClientIds.

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
An array of 1 or more Groups.

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
The Name of the SSE connection.

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

### System.Boolean
## NOTES

## RELATED LINKS
