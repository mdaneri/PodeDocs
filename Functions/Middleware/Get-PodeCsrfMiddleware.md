---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Middleware
schema: 2.0.0
---

# Get-PodeCsrfMiddleware

## SYNOPSIS
Returns adhoc CSRF CSRF verification Middleware, for use on Routes.

## SYNTAX

```
Get-PodeCsrfMiddleware [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns adhoc CSRF CSRF verification Middleware, for use on Routes.

## EXAMPLES

### EXAMPLE 1
```
$csrf = Get-PodeCsrfMiddleware
Add-PodeRoute -Method Get -Path '/cpu' -Middleware $csrf -ScriptBlock { /* logic */ }
```

## PARAMETERS

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

### System.Collections.Hashtable
## NOTES

## RELATED LINKS
