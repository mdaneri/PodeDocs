---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# Add-PodeAccessMiddleware

## SYNOPSIS
Adds an access method as global middleware.

## SYNTAX

```
Add-PodeAccessMiddleware [-Name] <String> [-Access] <String> [[-Route] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds an access method as global middleware.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeAccessMiddleware -Name 'GlobalAccess' -Access AccessName
```

### EXAMPLE 2
```
Add-PodeAccessMiddleware -Name 'GlobalAccess' -Access AccessName -Route '/api/*'
```

## PARAMETERS

### -Access
The Name of the Access method to use.

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

### -Name
The Name of the Middleware.

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

### -Route
A Route path for which Routes this Middleware should only be invoked against.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
