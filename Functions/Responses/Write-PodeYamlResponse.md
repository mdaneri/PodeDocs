---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeYamlResponse

## SYNOPSIS
Writes YAML data to the Response.

## SYNTAX

### Value (Default)
```
Write-PodeYamlResponse [-Value] <Object> [-ContentType <String>] [-Depth <Int32>] [-StatusCode <Int32>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Write-PodeYamlResponse -Path <String> [-ContentType <String>] [-StatusCode <Int32>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Writes YAML data to the Response, setting the content type accordingly.

## EXAMPLES

### EXAMPLE 1
```
Write-PodeYamlResponse -Value 'name: "Rick"'
```

### EXAMPLE 2
```
Write-PodeYamlResponse -Value @{ Name = 'Rick' } -StatusCode 201
```

### EXAMPLE 3
```
Write-PodeYamlResponse -Path 'E:/Files/Names.yaml'
```

## PARAMETERS

### -ContentType
Because YAML content has not yet an official content type.
one custom can be specified here (Default: 'application/yaml' )
https://www.rfc-editor.org/rfc/rfc9512

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Application/yaml
Accept pipeline input: False
Accept wildcard characters: False
```

### -Depth
The Depth to generate the YAML document - the larger this value the worse performance gets.

```yaml
Type: Int32
Parameter Sets: Value
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The path to a YAML file.

```yaml
Type: String
Parameter Sets: File
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
A String, PSObject, or HashTable value.
For non-string values, they will be converted to YAML.

```yaml
Type: Object
Parameter Sets: Value
Aliases:

Required: True
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
