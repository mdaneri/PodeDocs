---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeMarkdownResponse

## SYNOPSIS
Writes Markdown data to the Response.

## SYNTAX

### Value (Default)
```
Write-PodeMarkdownResponse [-Value] <Object> [-StatusCode <Int32>] [-AsHtml]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Write-PodeMarkdownResponse -Path <String> [-StatusCode <Int32>] [-AsHtml] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Writes Markdown data to the Response, with the option to render it as HTML.

## EXAMPLES

### EXAMPLE 1
```
Write-PodeMarkdownResponse -Value '# Hello, world!' -AsHtml
```

### EXAMPLE 2
```
Write-PodeMarkdownResponse -Path 'E:/Site/About.md'
```

## PARAMETERS

### -AsHtml
If supplied, the Markdown will be converted to HTML.
(This is only supported in PS7+)

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
The path to a Markdown file.

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
A String value.

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
