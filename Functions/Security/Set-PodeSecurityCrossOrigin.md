---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Security
schema: 2.0.0
---

# Set-PodeSecurityCrossOrigin

## SYNOPSIS
Removes definitions for the Cross-Origin headers.

## SYNTAX

```
Set-PodeSecurityCrossOrigin [[-Embed] <String>] [[-Open] <String>] [[-Resource] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Removes definitions for the Cross-Origin headers: Cross-Origin-Embedder-Policy, Cross-Origin-Opener-Policy, Cross-Origin-Resource-Policy

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSecurityCrossOrigin -Embed Require-Corp -Open Same-Origin -Resource Same-Origin
```

## PARAMETERS

### -Embed
Specifies a value for Cross-Origin-Embedder-Policy.

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

### -Open
Specifies a value for Cross-Origin-Opener-Policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### -Resource
Specifies a value for Cross-Origin-Resource-Policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
