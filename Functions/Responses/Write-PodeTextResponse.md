---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeTextResponse

## SYNOPSIS
Writes a String or a Byte\[\] to the Response.

## SYNTAX

### String (Default)
```
Write-PodeTextResponse [[-Value] <String>] [-ContentType <String>] [-MaxAge <Int32>] [-StatusCode <Int32>]
 [-Cache] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Bytes
```
Write-PodeTextResponse [-Bytes <Byte[]>] [-ContentType <String>] [-MaxAge <Int32>] [-StatusCode <Int32>]
 [-Cache] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Writes a String or a Byte\[\] to the Response, as some specified content type.
This value can also be cached.

## EXAMPLES

### EXAMPLE 1
```
Write-PodeTextResponse -Value 'Leeeeeerrrooooy Jeeeenkiiins!'
```

### EXAMPLE 2
```
Write-PodeTextResponse -Value '{"name": "Rick"}' -ContentType 'application/json'
```

### EXAMPLE 3
```
Write-PodeTextResponse -Bytes (Get-Content -Path ./some/image.png -Raw -AsByteStream) -Cache -MaxAge 1800
```

### EXAMPLE 4
```
Write-PodeTextResponse -Value 'Untitled Text Response' -StatusCode 418
```

## PARAMETERS

### -Bytes
An array of Bytes to write.

```yaml
Type: Byte[]
Parameter Sets: Bytes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cache
Should the value be cached by browsers, or not?

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

### -ContentType
The content type of the data being written.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Text/plain
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxAge
The maximum age to cache the value on the browser, in seconds.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3600
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

### -StatusCode
The status code to set against the response.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 200
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
A String value to write.

```yaml
Type: String
Parameter Sets: String
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
