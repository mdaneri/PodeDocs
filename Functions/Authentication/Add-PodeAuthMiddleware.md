---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Add-PodeAuthMiddleware

## SYNOPSIS
Adds an authentication method as global middleware.

## SYNTAX

```
Add-PodeAuthMiddleware [-Name] <String> [-Authentication] <String> [[-Route] <String>]
 [[-OADefinitionTag] <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds an authentication method as global middleware.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeAuthMiddleware -Name 'GlobalAuth' -Authentication AuthName
```

### EXAMPLE 2
```
Add-PodeAuthMiddleware -Name 'GlobalAuth' -Authentication AuthName -Route '/api/*'
```

## PARAMETERS

### -Authentication
The Name of the Authentication method to use.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Auth

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

### -OADefinitionTag
An array of string representing the unique tag for the API specification.
This tag helps in distinguishing between different versions or types of API specifications within the application.
Use this tag to reference the specific API documentation, schema, or version that your function interacts with.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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
