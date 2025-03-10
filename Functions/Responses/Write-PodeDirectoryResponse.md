---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeDirectoryResponse

## SYNOPSIS
Serves a directory listing as a web page.

## SYNTAX

```
Write-PodeDirectoryResponse [-Path] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The Write-PodeDirectoryResponse function generates an HTML response that lists the contents of a specified directory,
allowing for browsing of files and directories.
It supports both Windows and Unix-like environments by adjusting the
display of file attributes accordingly.
If the path is a directory, it generates a browsable HTML view; otherwise, it
serves the file directly.

## EXAMPLES

### EXAMPLE 1
```
Write-PodeDirectoryResponse -Path './static'
```

Generates and serves an HTML page that lists the contents of the './static' directory, allowing users to click through files and directories.

## PARAMETERS

### -Path
The path to the directory that should be displayed.
This path is resolved and used to generate a list of contents.

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
