---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: SSE
schema: 2.0.0
---

# Enable-PodeSseSigning

## SYNOPSIS
Enable the signing of SSE connection ClientIds.

## SYNTAX

```
Enable-PodeSseSigning [-Secret] <String> [-Strict] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Enable the signing of SSE connection ClientIds.

## EXAMPLES

### EXAMPLE 1
```
Enable-PodeSseSigning
```

### EXAMPLE 2
```
Enable-PodeSseSigning -Strict
```

### EXAMPLE 3
```
Enable-PodeSseSigning -Secret 'Sup3rS3cr37!' -Strict
```

### EXAMPLE 4
```
Enable-PodeSseSigning -Secret 'Sup3rS3cr37!'
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

### -Secret
A Secret to sign ClientIds, Get-PodeServerDefaultSecret can be used.

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

### -Strict
If supplied, the Secret will be extended using the client request's UserAgent and RemoteIPAddress.

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
