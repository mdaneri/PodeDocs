---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeXmlResponse

## SYNOPSIS
Writes XML data to the Response.

## SYNTAX

### Value (Default)
```
Write-PodeXmlResponse [-Value] <Object> [-Depth <Int32>] [-ContentType <String>] [-StatusCode <Int32>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Write-PodeXmlResponse -Path <String> [-ContentType <String>] [-StatusCode <Int32>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Writes XML data to the Response, setting the content type accordingly.

## EXAMPLES

### EXAMPLE 1
```
<name>Rick</name></root>'
```

### EXAMPLE 2
```
Write-PodeXmlResponse -Value @{ Name = 'Rick' } -StatusCode 201
```

### EXAMPLE 3
```
@(@{ Name = 'Rick' }, @{ Name = 'Don' }) | Write-PodeXmlResponse
```

### EXAMPLE 4
```
$users = @([PSCustomObject]@{
                Name = 'Rick'
            }, [PSCustomObject]@{
                Name = 'Don'
            }
        )
Write-PodeXmlResponse -Value $users
```

### EXAMPLE 5
```
@([PSCustomObject]@{
        Name = 'Rick'
    }, [PSCustomObject]@{
        Name = 'Don'
    }
) | Write-PodeXmlResponse
```

### EXAMPLE 6
```
Write-PodeXmlResponse -Path 'E:/Files/Names.xml'
```

## PARAMETERS

### -ContentType
Because XML content has not yet an official content type.
one custom can be specified here (Default: 'application/xml' )
https://www.rfc-editor.org/rfc/rfc3023

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Application/xml
Accept pipeline input: False
Accept wildcard characters: False
```

### -Depth
The Depth to generate the XML document - the larger this value the worse performance gets.

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
The path to an XML file.

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
