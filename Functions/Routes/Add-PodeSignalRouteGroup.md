---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Add-PodeSignalRouteGroup

## SYNOPSIS
Adds a Signal Route Group for multiple WebSockets.

## SYNTAX

```
Add-PodeSignalRouteGroup [[-Path] <String>] [-Routes] <ScriptBlock> [[-EndpointName] <String[]>]
 [[-IfExists] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a Signal Route Group for sharing values between multiple WebSockets.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeSignalRouteGroup -Path '/signals' -Routes { Add-PodeSignalRoute -Path '/signal1' -Etc }
```

## PARAMETERS

### -EndpointName
The EndpointName of an Endpoint(s) to use for the Signal Routes.

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

### -IfExists
Specifies what action to take when a Signal Route already exists.
(Default: Default)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The URI path to use as a base for the Signal Routes, that should be prepended.

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

### -Routes
A ScriptBlock for adding Signal Routes.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
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
