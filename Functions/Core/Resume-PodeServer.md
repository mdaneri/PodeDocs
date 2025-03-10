---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Resume-PodeServer

## SYNOPSIS
Resumes the Pode server from a suspended state.

## SYNTAX

```
Resume-PodeServer [[-Timeout] <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function resumes the Pode server, ensuring all associated runspaces are restored to their normal execution state.
It triggers the 'Resume' event, updates the server's suspended status, and clears the host for a refreshed console view.

## EXAMPLES

### EXAMPLE 1
```
Resume-PodeServer
# Resumes the Pode server after a suspension.
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
The maximum time, in seconds, to wait for each runspace to be recovered before timing out.
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
