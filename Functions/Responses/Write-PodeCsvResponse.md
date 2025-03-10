---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeCsvResponse

## SYNOPSIS
Writes CSV data to the Response.

## SYNTAX

### Value (Default)
```
Write-PodeCsvResponse [-Value] <Object> [-StatusCode <Int32>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### File
```
Write-PodeCsvResponse -Path <String> [-StatusCode <Int32>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Writes CSV data to the Response, setting the content type accordingly.

## EXAMPLES

### EXAMPLE 1
```
Write-PodeCsvResponse -Value "Name`nRick"
```

### EXAMPLE 2
```
Write-PodeCsvResponse -Value @{ Name = 'Rick' }
```

### EXAMPLE 3
```
Write-PodeCsvResponse -Path 'E:/Files/Names.csv'
```

## PARAMETERS

### -Path
The path to a CSV file.

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
