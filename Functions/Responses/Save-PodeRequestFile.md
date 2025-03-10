---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Save-PodeRequestFile

## SYNOPSIS
Saves any uploaded files on the Request to the File System.

## SYNTAX

```
Save-PodeRequestFile [-Key] <String> [[-Path] <String>] [[-FileName] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Saves any uploaded files on the Request to the File System.

## EXAMPLES

### EXAMPLE 1
```
Save-PodeRequestFile -Key 'avatar'
```

### EXAMPLE 2
```
Save-PodeRequestFile -Key 'avatar' -Path 'F:/Images'
```

### EXAMPLE 3
```
Save-PodeRequestFile -Key 'avatar' -Path 'F:/Images' -FileName 'icon.png'
```

## PARAMETERS

### -FileName
An optional FileName to save a specific files if multiple files were supplied in the Request.
By default, every file is saved.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Key
The name of the key within the $WebEvent's Data HashTable that stores the file names.

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

### -Path
The path to save files.
If this is a directory then the file name of the uploaded file will be used, but if this is a file path then that name is used instead.
If the Request has multiple files in, and you specify a file path, then all files will be saved to that one file path - overwriting each other.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: .
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
