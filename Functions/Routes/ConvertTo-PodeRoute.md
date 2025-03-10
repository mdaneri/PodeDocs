---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# ConvertTo-PodeRoute

## SYNOPSIS
Takes an array of Commands, or a Module, and converts them into Routes.

## SYNTAX

```
ConvertTo-PodeRoute [[-Commands] <String[]>] [-Module <String>] [-Method <String>] [-Path <String>]
 [-Middleware <Object[]>] [-Authentication <String>] [-Access <String>] [-Role <String[]>] [-Group <String[]>]
 [-Scope <String[]>] [-User <String[]>] [-AllowAnon] [-NoVerb] [-NoOpenApi]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Takes an array of Commands (Functions/Aliases), or a Module, and generates appropriate Routes for the commands.

## EXAMPLES

### EXAMPLE 1
```
ConvertTo-PodeRoute -Commands @('Get-ChildItem', 'Get-Host', 'Invoke-Expression') -Middleware { ... }
```

### EXAMPLE 2
```
ConvertTo-PodeRoute -Commands @('Get-ChildItem', 'Get-Host', 'Invoke-Expression') -Authentication AuthName
```

### EXAMPLE 3
```
ConvertTo-PodeRoute -Module Pester -Path '/api'
```

### EXAMPLE 4
```
ConvertTo-PodeRoute -Commands @('Invoke-Pester') -Module Pester
```

## PARAMETERS

### -Access
The name of an Access method which should be used as middleware on this Route.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowAnon
If supplied, the Route will allow anonymous access for non-authenticated users.

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

### -Authentication
The name of an Authentication method which should be used as middleware on this Route.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Auth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Commands
An array of Commands to convert - if a Module is supplied, these Commands must be present within that Module.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Group
One or more optional Groups that will be authorised to access this Route, when using Authentication with an Access method.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Method
An override HTTP method to use when generating the Routes.
If not supplied, Pode will make a best guess based on the Command's Verb.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Middleware
Like normal Routes, an array of Middleware that will be applied to all generated Routes.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Module
A Module whose exported commands will be converted.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoOpenApi
If supplied, no OpenAPI definitions will be generated for the routes created.

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

### -NoVerb
If supplied, the Command's Verb will not be included in the Route's path.

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

### -Path
An optional Path for the Route, to prepend before the Command Name and Module.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: /
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

### -Role
One or more optional Roles that will be authorised to access this Route, when using Authentication with an Access method.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
One or more optional Scopes that will be authorised to access this Route, when using Authentication with an Access method.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User
One or more optional Users that will be authorised to access this Route, when using Authentication with an Access method.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

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
