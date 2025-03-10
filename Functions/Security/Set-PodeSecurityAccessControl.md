---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Security
schema: 2.0.0
---

# Set-PodeSecurityAccessControl

## SYNOPSIS
Set definitions for Access-Control headers.

## SYNTAX

```
Set-PodeSecurityAccessControl [[-Origin] <String>] [[-Methods] <String[]>] [[-Headers] <String[]>]
 [[-Duration] <Int32>] [-Credentials] [-WithOptions] [-AuthorizationHeader] [-AutoHeaders] [-AutoMethods]
 [-CrossDomainXhrRequests] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Removes definitions for the Access-Control headers: Access-Control-Allow-Origin, Access-Control-Allow-Methods, Access-Control-Allow-Headers, Access-Control-Max-Age, Access-Control-Allow-Credentials

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSecurityAccessControl -Origin '*' -Methods '*' -Headers '*' -Duration 7200
```

## PARAMETERS

### -AuthorizationHeader
Add 'Authorization' to the headers list

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

### -AutoHeaders
Automatically populate the list of allowed Headers based on the OpenApi definition.
This parameter can works in conjuntion with CrossDomainXhrRequests,AuthorizationHeader and Headers (Headers cannot be '*').
By default add  'content-type' to the headers

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

### -AutoMethods
Automatically populate the list of allowed Methods based on the defined Routes.
This parameter can works in conjuntion with the parameter Methods, if Methods is not including '*'

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

### -Credentials
Specifies a value for Access-Control-Allow-Credentials

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

### -CrossDomainXhrRequests
Add 'x-requested-with' to the list of allowed headers
More info available here:
https://fetch.spec.whatwg.org/
https://learn.microsoft.com/en-us/aspnet/core/security/cors?view=aspnetcore-7.0#credentials-in-cross-origin-requests
https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

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

### -Duration
Specifies a value for Access-Control-Max-Age in seconds.
(Default: 7200)
Use a value of one for debugging any CORS related issues

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 7200
Accept pipeline input: False
Accept wildcard characters: False
```

### -Headers
Specifies a value for Access-Control-Allow-Headers.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Methods
Specifies a value for Access-Control-Allow-Methods.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Origin
Specifies a value for Access-Control-Allow-Origin.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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

### -WithOptions
If supplied, a global Options Route will be created.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
