---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Test-PodeSignalRoute

## SYNOPSIS
Test if a Signal Route already exists.

## SYNTAX

```
Test-PodeSignalRoute [-Path] <String> [[-EndpointName] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Test if a Signal Route already exists for a given Path.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeSignalRoute -Path '/message'
```

## PARAMETERS

### -EndpointName
The EndpointName of an Endpoint the Signal Route is bound against.

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
The URI path of the Signal Route.

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
