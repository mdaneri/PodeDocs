---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Set-PodeSseDefaultScope

## SYNOPSIS
Sets the default scope for new SSE connections.

## SYNTAX

```
Set-PodeSseDefaultScope [-Scope] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Sets the default scope for new SSE connections.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSseDefaultScope -Scope Local
```

### EXAMPLE 2
```
Set-PodeSseDefaultScope -Scope Global
```

## PARAMETERS

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

### -Scope
The default Scope for new SSE connections, either Local or Global.
- If the Scope is Local, then new SSE connections will only be opened for the duration of the request to a Route that configured it.
- If the Scope is Global, then new SSE connections will be cached internally so events can be sent to the connection from Tasks, Timers, and other Routes, etc.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
