---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Headers
schema: 2.0.0
---

# Test-PodeHeaderSigned

## SYNOPSIS
Tests if a header on the Request is validly signed.

## SYNTAX

```
Test-PodeHeaderSigned [-Name] <String> [[-Secret] <String>] [-Strict] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Tests if a header on the Request is validly signed, by attempting to unsign it using some secret.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeHeaderSigned -Name 'X-Header-Name' -Secret 'hunter2'
```

## PARAMETERS

### -Name
The name of the header to test.

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
A secret to use for attempting to unsign the header's value.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Boolean
## NOTES

## RELATED LINKS
