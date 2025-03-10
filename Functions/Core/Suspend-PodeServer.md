---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Suspend-PodeServer

## SYNOPSIS
Suspends the Pode server and its runspaces.

## SYNTAX

```
Suspend-PodeServer [[-Timeout] <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function suspends the Pode server by pausing all associated runspaces and ensuring they enter a debug state.
It triggers the 'Suspend' event, updates the server's suspended status, and provides feedback during the suspension process.

## EXAMPLES

### EXAMPLE 1
```
Suspend-PodeServer
# Suspends the Pode server with a timeout of 60 seconds.
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

### -Timeout
The maximum time, in seconds, to wait for each runspace to be suspended before timing out.
Default is 30 seconds.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
