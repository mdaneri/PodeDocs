---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Set-PodeResponseAttachment

## SYNOPSIS
Attaches a file onto the Response for downloading.

## SYNTAX

```
Set-PodeResponseAttachment [-Path] <String> [-ContentType <String>] [-EndpointName <String>] [-FileBrowser]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Attaches a file from the "/public", and static Routes, onto the Response for downloading.
If the supplied path is not in the Static Routes but is a literal/relative path, then this file is used instead.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeResponseAttachment -Path 'downloads/installer.exe'
```

### EXAMPLE 2
```
Set-PodeResponseAttachment -Path './image.png'
```

### EXAMPLE 3
```
Set-PodeResponseAttachment -Path 'c:/content/accounts.xlsx'
```

### EXAMPLE 4
```
Set-PodeResponseAttachment -Path './data.txt' -ContentType 'application/json'
```

### EXAMPLE 5
```
Set-PodeResponseAttachment -Path '/assets/data.txt' -EndpointName 'Example'
```

## PARAMETERS

### -ContentType
Manually specify the content type of the response rather than inferring it from the attachment's file extension.
The supplied value must match the valid ContentType format, e.g.
application/json

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

### -EndpointName
Optional EndpointName that the static route was creating under.

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

### -Path
The Path to a static file relative to the "/public" directory, or a static Route.
If the supplied Path doesn't match any custom static Route, then Pode will look in the "/public" directory.
Failing this, if the file path exists as a literal/relative file, then this file is used as a fall back.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
