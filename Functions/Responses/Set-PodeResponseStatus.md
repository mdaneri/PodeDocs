---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Set-PodeResponseStatus

## SYNOPSIS
Sets the Status Code of the Response, and controls rendering error pages.

## SYNTAX

```
Set-PodeResponseStatus [-Code] <Int32> [[-Description] <String>] [[-Exception] <Object>]
 [[-ContentType] <String>] [-NoErrorPage] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Sets the Status Code of the Response, and controls rendering error pages.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeResponseStatus -Code 404
```

### EXAMPLE 2
```
Set-PodeResponseStatus -Code 500 -Exception $_.Exception
```

### EXAMPLE 3
```
Set-PodeResponseStatus -Code 500 -Exception $_.Exception -ContentType 'application/json'
```

## PARAMETERS

### -Code
The Status Code to set on the Response.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentType
The content type of the error page to use.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
An optional Status Description.

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

### -Exception
An exception to use when detailing error information on error pages.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoErrorPage
Don't render an error page when the Status Code is 400+.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
