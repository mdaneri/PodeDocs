---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Headers
schema: 2.0.0
---

# Get-PodeHeader

## SYNOPSIS
Retrieves the value of a specified header from the incoming request.

## SYNTAX

### BuiltIn (Default)
```
Get-PodeHeader -Name <String> [-Secret <String>] [-Strict] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Deserialize
```
Get-PodeHeader -Name <String> [-Explode] [-Deserialize] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
The \`Get-PodeHeader\` function retrieves the value of a specified header from the incoming request.
It supports deserialization of header values and can optionally unsign the header using a specified secret.
The unsigning process can be further secured with the client's UserAgent and RemoteIPAddress if \`-Strict\` is specified.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeHeader -Name 'X-AuthToken'
Retrieves the value of the 'X-AuthToken' header from the request.
```

### EXAMPLE 2
```
Get-PodeHeader -Name 'X-SerializedHeader' -Deserialize -Explode
Retrieves and deserializes the value of the 'X-SerializedHeader' header, exploding arrays if present.
```

### EXAMPLE 3
```
Get-PodeHeader -Name 'X-AuthToken' -Secret 'MySecret' -Strict
Retrieves and unsigns the 'X-AuthToken' header using the specified secret, extending it with UserAgent and
RemoteIPAddress information for added security.
```

## PARAMETERS

### -Deserialize
Indicates that the retrieved header value should be deserialized.
When this switch is used, the value will be
interpreted based on the provided deserialization options.
This parameter is mandatory in the 'Deserialize' parameter set.

```yaml
Type: SwitchParameter
Parameter Sets: Deserialize
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Explode
Specifies whether the deserialization process should explode arrays in the header value.
This is useful when
handling comma-separated values within the header.
Applicable only when the \`-Deserialize\` switch is used.

```yaml
Type: SwitchParameter
Parameter Sets: Deserialize
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the header to retrieve.
This parameter is mandatory.

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

### -Secret
The secret used to unsign the header's value.
This option is useful when working with signed headers to ensure
the integrity and authenticity of the value.
Applicable only in the 'BuiltIn' parameter set.

```yaml
Type: String
Parameter Sets: BuiltIn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Strict
If specified, the secret is extended using the client's UserAgent and RemoteIPAddress, providing an additional
layer of security during the unsigning process.
Applicable only in the 'BuiltIn' parameter set.

```yaml
Type: SwitchParameter
Parameter Sets: BuiltIn
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
This function should be used within a route's script block in a Pode server.
The \`-Deserialize\` switch enables
advanced handling of serialized header values, while the \`-Secret\` and \`-Strict\` options provide secure unsigning
capabilities for signed headers.

## RELATED LINKS
