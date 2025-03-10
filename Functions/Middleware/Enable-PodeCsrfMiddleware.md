---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Middleware
schema: 2.0.0
---

# Enable-PodeCsrfMiddleware

## SYNOPSIS
Enables Middleware for verifying CSRF tokens on Requests.

## SYNTAX

```
Enable-PodeCsrfMiddleware [-IgnoreMethods <String[]>] [-Secret <String>] [-UseCookies]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Enables Middleware for verifying CSRF tokens on Requests, with configurable HTTP methods to ignore verification.

## EXAMPLES

### EXAMPLE 1
```
Enable-PodeCsrfMiddleware -IgnoreMethods @('Get', 'Trace')
```

### EXAMPLE 2
```
Enable-PodeCsrfMiddleware -Secret 'some-secret' -UseCookies
```

## PARAMETERS

### -IgnoreMethods
An array of HTTP methods to ignore CSRF verification.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: @('Get', 'Head', 'Options', 'Trace')
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

### -Secret
A secret to use when signing cookies - for when using CSRF with cookies.

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

### -UseCookies
If supplied, CSRF will used cookies rather than sessions.

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
