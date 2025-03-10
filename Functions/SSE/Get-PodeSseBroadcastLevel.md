---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Get-PodeSseBroadcastLevel

## SYNOPSIS
Retrieve the broadcast level for an SSE connection Name.

## SYNTAX

```
Get-PodeSseBroadcastLevel [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Retrieve the broadcast level for an SSE connection Name.
If one hasn't been set explicitly then the base level will be checked.
If no broadcasting level have been set at all, then the "Name" level will be returned.

## EXAMPLES

### EXAMPLE 1
```
$level = Get-PodeSseBroadcastLevel -Name 'Actions'
```

## PARAMETERS

### -Name
The Name of an SSE connection.

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

### System.String
## NOTES

## RELATED LINKS
