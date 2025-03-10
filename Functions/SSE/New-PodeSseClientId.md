---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# New-PodeSseClientId

## SYNOPSIS
Generate a new SSE connection ClientId.

## SYNTAX

```
New-PodeSseClientId [[-ClientId] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Generate a new SSE connection ClientId, which will be signed if signing enabled.

## EXAMPLES

### EXAMPLE 1
```
$clientId = New-PodeSseClientId
```

### EXAMPLE 2
```
$clientId = New-PodeSseClientId -ClientId 'my-client-id'
```

### EXAMPLE 3
```
$clientId = New-PodeSseClientId -ClientId 's:my-already-signed-client-id.uvG49LcojTMuJ0l4yzBzr6jCqEV8gGC/0YgsYU1QEuQ='
```

## PARAMETERS

### -ClientId
An optional SSE connection ClientId to use, if a custom ClientId is needed and required to be signed.

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
