---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Add-PodeStaticRoute

## SYNOPSIS
Add a static Route for rendering static content.

## SYNTAX

```
Add-PodeStaticRoute [-Path] <String> [-Source] <String> [[-Middleware] <Object[]>] [[-EndpointName] <String[]>]
 [[-ContentType] <String>] [[-TransferEncoding] <String>] [[-Defaults] <String[]>]
 [[-ErrorContentType] <String>] [[-Authentication] <String>] [[-Access] <String>] [[-IfExists] <String>]
 [[-Role] <String[]>] [[-Group] <String[]>] [[-Scope] <String[]>] [[-User] <String[]>] [-AllowAnon]
 [-DownloadOnly] [-FileBrowser] [-PassThru] [-RedirectToDefault] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Add a static Route for rendering static content.
You can also define default pages to display.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeStaticRoute -Path '/assets' -Source './assets'
```

### EXAMPLE 2
```
Add-PodeStaticRoute -Path '/assets' -Source './assets' -Defaults @('index.html')
```

### EXAMPLE 3
```
Add-PodeStaticRoute -Path '/installers' -Source './exes' -DownloadOnly
```

### EXAMPLE 4
```
Add-PodeStaticRoute -Path '/assets' -Source './assets' -Defaults @('index.html') -RedirectToDefault
```

## PARAMETERS

### -Access
The name of an Access method which should be used as middleware on this Route.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowAnon
If supplied, the static route will allow anonymous access for non-authenticated users.

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
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentType
The content type the static Route should use when parsing any payloads.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Defaults
An array of default pages to display, such as 'index.html'.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DownloadOnly
When supplied, all static content on this Route will be attached as downloads - rather than rendered.

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
The EndpointName of an Endpoint(s) to bind the static Route against.

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

### -ErrorContentType
The content type of any error pages that may get returned.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileBrowser
If supplied, when the path is a folder, instead of returning 404, will return A browsable content of the directory.

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

### -Group
One or more optional Groups that will be authorised to access this Route, when using Authentication with an Access method.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IfExists
Specifies what action to take when a Static Route already exists.
(Default: Default)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -Middleware
An array of ScriptBlocks for optional Middleware.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
If supplied, the static route created will be returned so it can be passed through a pipe.

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
The URI path for the static Route.

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

### -RedirectToDefault
If supplied, the user will be redirected to the default page if found instead of the page being rendered as the folder path.

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

### -Role
One or more optional Roles that will be authorised to access this Route, when using Authentication with an Access method.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
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
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source
The literal, or relative, path to the directory that contains the static content.

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

### -TransferEncoding
The transfer encoding the static Route should use when parsing any payloads.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
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
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object[]
## NOTES

## RELATED LINKS
