---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Get-PodeServerDefaultSecret

## SYNOPSIS
A default server secret that can be for signing values like Session, Cookies, or SSE IDs.

## SYNTAX

```
Get-PodeServerDefaultSecret [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
A default server secret that can be for signing values like Session, Cookies, or SSE IDs.
This secret is regenerated
on every server start and restart.

## EXAMPLES

### EXAMPLE 1
```
$secret = Get-PodeServerDefaultSecret
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

## NOTES

## RELATED LINKS
