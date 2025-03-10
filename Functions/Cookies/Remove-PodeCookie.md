---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Cookies
schema: 2.0.0
---

# Remove-PodeCookie

## SYNOPSIS
Removes a cookie from the Response.

## SYNTAX

```
Remove-PodeCookie [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Removes a cookie from the Response, this is done by immediately expiring the cookie and flagging it for discard.

## EXAMPLES

### EXAMPLE 1
```
Remove-PodeCookie -Name 'Views'
```

## PARAMETERS

### -Name
The name of the cookie to be removed.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
