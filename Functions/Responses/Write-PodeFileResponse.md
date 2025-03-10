---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeFileResponse

## SYNOPSIS
Renders the content of a static, or dynamic, file on the Response.

## SYNTAX

```
Write-PodeFileResponse [-Path] <String> [-Data <Object>] [-ContentType <String>] [-MaxAge <Int32>]
 [-StatusCode <Int32>] [-Cache] [-FileBrowser] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Renders the content of a static, or dynamic, file on the Response.
You can set browser's to cache the content, and also override the file's content type.

## EXAMPLES

### EXAMPLE 1
```
Write-PodeFileResponse -Path 'C:/Files/Stuff.txt'
```

### EXAMPLE 2
```
Write-PodeFileResponse -Path 'C:/Files/Stuff.txt' -Cache -MaxAge 1800
```

### EXAMPLE 3
```
Write-PodeFileResponse -Path 'C:/Files/Stuff.txt' -ContentType 'application/json'
```

### EXAMPLE 4
```
Write-PodeFileResponse -Path 'C:/Views/Index.pode' -Data @{ Counter = 2 }
```

### EXAMPLE 5
```
Write-PodeFileResponse -Path 'C:/Files/Stuff.txt' -StatusCode 201
```

### EXAMPLE 6
```
Write-PodeFileResponse -Path 'C:/Files/' -FileBrowser
```

## PARAMETERS

### -Cache
Should the file's content be cached by browsers, or not?

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
The content type of the file's contents - this overrides the file's extension.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Data
A HashTable of dynamic data to supply to a dynamic file.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: @{}
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileBrowser
If the path is a folder, instead of returning 404, will return A browsable content of the directory.

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

### -MaxAge
The maximum age to cache the file's content on the browser, in seconds.

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

### -Path
The path to a file.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
