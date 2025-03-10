---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Security
schema: 2.0.0
---

# Set-PodeSecurity

## SYNOPSIS
Sets inbuilt definitions for security headers.

## SYNTAX

```
Set-PodeSecurity [-Type] <String> [-UseHsts] [-XssBlock] [-CspReportOnly] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Sets inbuilt definitions for security headers, in either Simple or Strict types.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSecurity -Type Simple
```

### EXAMPLE 2
```
Set-PodeSecurity -Type Strict -UseHsts
```

## PARAMETERS

### -CspReportOnly
If supplied, the Content-Security-Policy header will be set as the Content-Security-Policy-Report-Only header.

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

### -Type
The Type of security to use.

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

### -UseHsts
If supplied, the Strict-Transport-Security header will be set.

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

### -XssBlock
If supplied, the X-XSS-Protection header will be set to blocking mode.
(Default: Off)

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
