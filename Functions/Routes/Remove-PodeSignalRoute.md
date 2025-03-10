---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Remove-PodeSignalRoute

## SYNOPSIS
Remove a specific Signal Route.

## SYNTAX

```
Remove-PodeSignalRoute [-Path] <String> [[-EndpointName] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Remove a specific Signal Route.

## EXAMPLES

### EXAMPLE 1
```
Remove-PodeSignalRoute -Route '/message'
```

## PARAMETERS

### -EndpointName
The EndpointName of an Endpoint(s) bound to the Signal Route to be removed.

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

### -Path
The path of the Signal Route to remove.

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
