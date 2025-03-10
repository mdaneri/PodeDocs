---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Headers
schema: 2.0.0
---

# Set-PodeHeader

## SYNOPSIS
Sets a header on the Response, clearing all current values for the header.

## SYNTAX

```
Set-PodeHeader [-Name] <String> [-Value] <String> [[-Secret] <String>] [-Strict]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Sets a header on the Response, clearing all current values for the header.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeHeader -Name 'X-AuthToken' -Value 'AA-BB-CC-33'
```

## PARAMETERS

### -Name
The name of the header.

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

### -Secret
If supplied, the secret with which to sign the header's value.

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

### -Value
The value to set against the header.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
