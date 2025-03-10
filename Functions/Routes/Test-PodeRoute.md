---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Test-PodeRoute

## SYNOPSIS
Test if a Route already exists.

## SYNTAX

```
Test-PodeRoute [-Method] <String> [-Path] <String> [[-EndpointName] <String>] [-CheckWildcard]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Test if a Route already exists for a given Method and Path.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeRoute -Method Post -Path '/example'
```

### EXAMPLE 2
```
Test-PodeRoute -Method Post -Path '/example' -CheckWildcard
```

### EXAMPLE 3
```
Test-PodeRoute -Method Get -Path '/example/:exampleId' -CheckWildcard
```

## PARAMETERS

### -CheckWildcard
If supplied, Pode will check for the Route on the Method first, and then check for the Route on the '*' Method.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
The EndpointName of an Endpoint the Route is bound against.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
The HTTP Method of the Route.

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

### -Path
The URI path of the Route.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
