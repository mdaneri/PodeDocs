---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Add-PodeRoute

## SYNOPSIS
Adds a Route for a specific HTTP Method(s).

## SYNTAX

### Script (Default)
```
Add-PodeRoute -Method <String[]> -Path <String> [-Middleware <Object[]>] [-ScriptBlock <ScriptBlock>]
 [-EndpointName <String[]>] [-ContentType <String>] [-TransferEncoding <String>] [-ErrorContentType <String>]
 [-ArgumentList <Object[]>] [-Authentication <String>] [-Access <String>] [-IfExists <String>]
 [-Role <String[]>] [-Group <String[]>] [-Scope <String[]>] [-User <String[]>] [-AllowAnon] [-Login] [-Logout]
 [-OAResponses <Hashtable>] [-OAReference <String>] [-PassThru] [-OADefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodeRoute -Method <String[]> -Path <String> [-Middleware <Object[]>] [-EndpointName <String[]>]
 [-ContentType <String>] [-TransferEncoding <String>] [-ErrorContentType <String>] -FilePath <String>
 [-ArgumentList <Object[]>] [-Authentication <String>] [-Access <String>] [-IfExists <String>]
 [-Role <String[]>] [-Group <String[]>] [-Scope <String[]>] [-User <String[]>] [-AllowAnon] [-Login] [-Logout]
 [-OAResponses <Hashtable>] [-OAReference <String>] [-PassThru] [-OADefinitionTag <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a Route for a specific HTTP Method(s), with path, that when called with invoke any logic and/or Middleware.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeRoute -Method Get -Path '/' -ScriptBlock { /* logic */ }
```

### EXAMPLE 2
```
Add-PodeRoute -Method Post -Path '/users/:userId/message' -Middleware (Get-PodeCsrfMiddleware) -ScriptBlock { /* logic */ }
```

### EXAMPLE 3
```
Add-PodeRoute -Method Post -Path '/user' -ContentType 'application/json' -ScriptBlock { /* logic */ }
```

### EXAMPLE 4
```
Add-PodeRoute -Method Post -Path '/user' -ContentType 'application/json' -TransferEncoding gzip -ScriptBlock { /* logic */ }
```

### EXAMPLE 5
```
Add-PodeRoute -Method Get -Path '/api/cpu' -ErrorContentType 'application/json' -ScriptBlock { /* logic */ }
```

### EXAMPLE 6
```
Add-PodeRoute -Method Get -Path '/' -ScriptBlock { /* logic */ } -ArgumentList 'arg1', 'arg2'
```

### EXAMPLE 7
```
Add-PodeRoute -Method Get -Path '/' -Role 'Developer', 'QA' -ScriptBlock { /* logic */ }
```

### EXAMPLE 8
```
$Responses = New-PodeOAResponse -StatusCode 400 -Description 'Invalid username supplied' |
            New-PodeOAResponse -StatusCode 404 -Description 'User not found' |
            New-PodeOAResponse -StatusCode 405 -Description 'Invalid Input'
```

Add-PodeRoute -PassThru -Method Put -Path '/user/:username' -OAResponses $Responses -ScriptBlock {
            #code is going here
        }

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

### -ArgumentList
An array of arguments to supply to the Route's ScriptBlock.

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

### -ContentType
The content type the Route should use when parsing any payloads.

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

### -EndpointName
The EndpointName of an Endpoint(s) this Route should be bound against.

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

### -ErrorContentType
The content type of any error pages that may get returned.

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

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the Route's main logic.

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

### -IfExists
Specifies what action to take when a Route already exists.
(Default: Default)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -Login
If supplied, the Route will be flagged to Authentication as being a Route that handles user logins.

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

### -Logout
If supplied, the Route will be flagged to Authentication as being a Route that handles users logging out.

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

### -Method
The HTTP Method of this Route, multiple can be supplied.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OADefinitionTag
An Array of strings representing the unique tag for the API specification.
This tag helps in distinguishing between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

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

### -OAReference
A reference to OpenAPI reusable pathItem component created with Add-PodeOAComponentPathItem

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

### -OAResponses
An alternative way to associate OpenApi responses unsing New-PodeOAResponse instead of piping multiple Add-PodeOAResponse

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

### -PassThru
If supplied, the route created will be returned so it can be passed through a pipe.

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
The URI path for the Route.

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
A ScriptBlock for the Route's main logic.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TransferEncoding
The transfer encoding the Route should use when parsing any payloads.

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

### System.Object[]
## NOTES

## RELATED LINKS
