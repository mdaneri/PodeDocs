---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Remove-PodeOAResponse

## SYNOPSIS
Remove a response definition from the supplied route.

## SYNTAX

```
Remove-PodeOAResponse [-Route] <Hashtable[]> [-StatusCode] <Int32> [-Default] [-PassThru]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Remove a response definition from the supplied route.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeRoute -PassThru | Remove-PodeOAResponse -StatusCode 200
```

### EXAMPLE 2
```
Add-PodeRoute -PassThru | Remove-PodeOAResponse -StatusCode 201 -Default
```

## PARAMETERS

### -Default
If supplied, the response will be used as a default response - this overrides the StatusCode supplied.

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

### -PassThru
If supplied, the route passed in will be returned for further chaining.

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

### -Route
The route to remove the response definition, usually from -PassThru on Add-PodeRoute.

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
The HTTP StatusCode for the response to remove.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable[]
## NOTES

## RELATED LINKS
