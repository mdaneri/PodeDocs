---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Add-PodePage

## SYNOPSIS
Helper function to generate simple GET routes.

## SYNTAX

### ScriptBlock (Default)
```
Add-PodePage -Name <String> -ScriptBlock <ScriptBlock> [-Data <Hashtable>] [-Path <String>]
 [-Middleware <Object[]>] [-Authentication <String>] [-Access <String>] [-Role <String[]>] [-Group <String[]>]
 [-Scope <String[]>] [-User <String[]>] [-AllowAnon] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodePage -Name <String> -FilePath <String> [-Data <Hashtable>] [-Path <String>] [-Middleware <Object[]>]
 [-Authentication <String>] [-Access <String>] [-Role <String[]>] [-Group <String[]>] [-Scope <String[]>]
 [-User <String[]>] [-AllowAnon] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### View
```
Add-PodePage -Name <String> -View <String> [-Data <Hashtable>] [-Path <String>] [-Middleware <Object[]>]
 [-Authentication <String>] [-Access <String>] [-Role <String[]>] [-Group <String[]>] [-Scope <String[]>]
 [-User <String[]>] [-AllowAnon] [-FlashMessages] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Helper function to generate simple GET routes from ScritpBlocks, Files, and Views.
The output is always rendered as HTML.

## EXAMPLES

### EXAMPLE 1
```
Add-PodePage -Name Services -ScriptBlock { Get-Service }
```

### EXAMPLE 2
```
Add-PodePage -Name Index -View 'index'
```

### EXAMPLE 3
```
Add-PodePage -Name About -FilePath '.\views\about.pode' -Data @{ Date = [DateTime]::UtcNow }
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
If supplied, the Page will allow anonymous access for non-authenticated users.

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

### -Data
A hashtable of Data to supply to a Dynamic File/View, or to be splatted as arguments for the ScriptBlock.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
A FilePath, literal or relative, to a valid HTML file.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FlashMessages
If supplied, Views will have any flash messages supplied to them for rendering.

```yaml
Type: SwitchParameter
Parameter Sets: View
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

### -Name
A unique name for the page, that will be used in the Path for the route.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
An optional Path for the Route, to prepend before the Name.

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

### -ScriptBlock
A ScriptBlock to invoke, where any results will be converted to HTML.

```yaml
Type: ScriptBlock
Parameter Sets: ScriptBlock
Aliases:

Required: True
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

### -View
The name of a View to render, this can be HTML or Dynamic.

```yaml
Type: String
Parameter Sets: View
Aliases:

Required: True
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
