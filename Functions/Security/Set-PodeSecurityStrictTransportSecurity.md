---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Security
schema: 2.0.0
---

# Set-PodeSecurityStrictTransportSecurity

## SYNOPSIS
Set a value for the Strict-Transport-Security header.

## SYNTAX

```
Set-PodeSecurityStrictTransportSecurity [[-Duration] <Int32>] [-IncludeSubDomains]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Set a value for the Strict-Transport-Security header.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSecurityStrictTransportSecurity -Duration 86400 -IncludeSubDomains
```

## PARAMETERS

### -Duration
The Duration the browser to respect the header in seconds.
(Default: 1 year)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: 31536000
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeSubDomains
If supplied, the header will have includeSubDomains.

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
