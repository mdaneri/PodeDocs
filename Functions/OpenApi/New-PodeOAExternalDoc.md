---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# New-PodeOAExternalDoc

## SYNOPSIS
Define an external docs reference.

## SYNTAX

```
New-PodeOAExternalDoc [-Url] <Object> [[-Description] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Define an external docs reference.

## EXAMPLES

### EXAMPLE 1
```
$swaggerDoc = New-PodeOAExternalDoc  -Description 'Find out more about Swagger' -Url 'http://swagger.io'
```

Add-PodeRoute -PassThru | Set-PodeOARouteInfo -Summary 'A quick summary' -Tags 'Admin' -ExternalDoc $swaggerDoc

### EXAMPLE 2
```
$swaggerDoc = New-PodeOAExternalDoc    -Description 'Find out more about Swagger' -Url 'http://swagger.io'
Add-PodeOATag -Name 'user' -Description 'Operations about user' -ExternalDoc $swaggerDoc
```

## PARAMETERS

### -Description
A Description of the external documentation.

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

### -Url
The link to the external documentation

```yaml
Type: Object
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
