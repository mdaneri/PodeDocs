---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Headers
schema: 2.0.0
---

# Add-PodeHeaderBulk

## SYNOPSIS
Appends multiple headers against the Response.

## SYNTAX

```
Add-PodeHeaderBulk [-Values] <Hashtable> [[-Secret] <String>] [-Strict] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Appends multiple headers against the Response.
If the current context is serverless, then this function acts like Set-PodeHeaderBulk.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeHeaderBulk -Values @{ Name1 = 'Value1'; Name2 = 'Value2' }
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
If supplied, the secret with which to sign the header values.

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

### -Values
A hashtable of headers to be appended.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
