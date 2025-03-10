---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Cookies
schema: 2.0.0
---

# Update-PodeCookieExpiry

## SYNOPSIS
Updates the exipry date of a cookie on the Response.

## SYNTAX

### Duration (Default)
```
Update-PodeCookieExpiry -Name <String> [-Duration <Int32>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### ExpiryDate
```
Update-PodeCookieExpiry -Name <String> [-ExpiryDate <DateTime>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Updates the exipry date of a cookie on the Response.
This can either be done by suppling a duration, or and explicit expiry date.

## EXAMPLES

### EXAMPLE 1
```
Update-PodeCookieExpiry -Name  'Views' -Duration 1800
```

### EXAMPLE 2
```
Update-PodeCookieExpiry -Name  'Views' -ExpiryDate ([datetime]::UtcNow.AddSeconds(1800))
```

## PARAMETERS

### -Duration
The duration, in seconds, to extend the cookie's expiry.

```yaml
Type: Int32
Parameter Sets: Duration
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryDate
An explicit expiry date for the cookie.

```yaml
Type: DateTime
Parameter Sets: ExpiryDate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the cookie to extend.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable
## NOTES

## RELATED LINKS
