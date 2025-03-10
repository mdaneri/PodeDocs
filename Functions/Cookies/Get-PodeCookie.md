---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Cookies
schema: 2.0.0
---

# Get-PodeCookie

## SYNOPSIS
Retrieves a specified cookie from the incoming request.

## SYNTAX

### BuiltIn (Default)
```
Get-PodeCookie -Name <String> [-Secret <String>] [-Strict] [-Raw] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Deserialize
```
Get-PodeCookie -Name <String> [-NoExplode] [-Deserialize] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
The \`Get-PodeCookie\` function retrieves a cookie from the incoming request.
It can unsign the cookie's value using a specified secret, which can be extended with the client request's UserAgent and RemoteIPAddress if \`-Strict\` is specified.
The function also allows for returning the raw .NET Cookie object for direct manipulation or deserializing serialized cookie values for more complex handling.

## EXAMPLES

### EXAMPLE 1
```
Get-PodeCookie -Name 'Views'
Retrieves the value of the 'Views' cookie from the request.
```

### EXAMPLE 2
```
Get-PodeCookie -Name 'Views' -Secret 'hunter2'
Retrieves and unsigns the 'Views' cookie using the specified secret.
```

### EXAMPLE 3
```
Get-PodeCookie -Name 'Session' -Deserialize -NoExplode
Retrieves and deserializes the 'Session' cookie value without exploding arrays.
```

### EXAMPLE 4
```
Get-PodeCookie -Name 'AuthToken' -Raw
Retrieves the raw .NET Cookie object for the 'AuthToken' cookie, allowing for direct manipulation.
```

## PARAMETERS

### -Deserialize
Indicates that the retrieved cookie value should be deserialized.
When this switch is used, the value will be
interpreted based on the deserialization options provided.
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

### -Name
The name of the cookie to retrieve.
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

### -NoExplode
Prevents deserialization from exploding arrays in the cookie value, which is useful when handling comma-separated
values without expanding them into arrays.
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

### -Raw
If specified, the cookie returned will be the raw .NET Cookie object, allowing for direct manipulation of
the cookie.
This is useful for scenarios where the full cookie object is needed.
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

### -Secret
The secret used to unsign the cookie's value, ensuring the integrity and authenticity of the cookie data.
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
If specified, the secret is extended using the client's UserAgent and RemoteIPAddress, adding an extra layer of
security when unsigning the cookie.
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
The \`-Deserialize\` switch provides
advanced handling of serialized cookie values, while the \`-Secret\` and \`-Strict\` options offer secure methods for
unsigning cookies.

## RELATED LINKS
