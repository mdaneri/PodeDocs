---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Write-PodeHost

## SYNOPSIS
Writes an object to the Host.

## SYNTAX

### inbuilt (Default)
```
Write-PodeHost [[-Object] <Object>] [-ForegroundColor <ConsoleColor>] [-NoNewLine] [-Force]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### object
```
Write-PodeHost [[-Object] <Object>] [-ForegroundColor <ConsoleColor>] [-NoNewLine] [-Explode] [-ShowType]
 [-Label <String>] [-Force] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Writes an object to the Host.
It's advised to use this function, so that any output respects the -Quiet flag of the server.

## EXAMPLES

### EXAMPLE 1
```
'Some output' | Write-PodeHost -ForegroundColor Cyan
```

## PARAMETERS

### -Explode
Show the object content

```yaml
Type: SwitchParameter
Parameter Sets: object
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Overrides the -Quiet flag of the server.

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

### -ForegroundColor
An optional foreground colour.

```yaml
Type: ConsoleColor
Parameter Sets: (All)
Aliases:
Accepted values: Black, DarkBlue, DarkGreen, DarkCyan, DarkRed, DarkMagenta, DarkYellow, Gray, DarkGray, Blue, Green, Cyan, Red, Magenta, Yellow, White

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Label
Show a label for the object

```yaml
Type: String
Parameter Sets: object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoNewLine
Whether or not to write a new line.

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

### -Object
The object to write.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: Message

Required: False
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

### -ShowType
Show the Object Type

```yaml
Type: SwitchParameter
Parameter Sets: object
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

## RELATED LINKS
