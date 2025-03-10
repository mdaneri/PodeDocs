---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Test-PodeSseClientIdValid

## SYNOPSIS
Test if an SSE connection ClientId is valid.

## SYNTAX

```
Test-PodeSseClientIdValid [[-ClientId] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Test if an SSE connection ClientId, passed or from $WebEvent, is valid.
A ClientId is valid if it's not signed and we're not signing ClientIds,
or if we are signing ClientIds and the ClientId is validly signed.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeSseClientIdValid) { ... }
```

### EXAMPLE 2
```
if (Test-PodeSseClientIdValid -ClientId 'my-client-id') { ... }
```

## PARAMETERS

### -ClientId
An optional SSE connection ClientId, if not supplied it will be retrieved from $WebEvent.

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

### System.Boolean
## NOTES

## RELATED LINKS
