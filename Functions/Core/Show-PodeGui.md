---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Show-PodeGui

## SYNOPSIS
Opens a Web Server up as a Desktop Application.

## SYNTAX

```
Show-PodeGui [-Title] <String> [[-Icon] <String>] [[-WindowState] <String>] [[-WindowStyle] <String>]
 [[-ResizeMode] <String>] [[-Height] <Int32>] [[-Width] <Int32>] [[-EndpointName] <String>] [-HideFromTaskbar]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Opens a Web Server up as a Desktop Application.

## EXAMPLES

### EXAMPLE 1
```
Show-PodeGui -Title 'MyApplication' -WindowState 'Maximized'
```

## PARAMETERS

### -EndpointName
The specific endpoint name to use, if you are listening on multiple endpoints.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Height
The height of the window.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -HideFromTaskbar
Stops the Application from appearing on the taskbar.

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

### -Icon
A path to an icon image for the Application.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### -ResizeMode
Specifies if the Application's window is resizable.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: CanResize
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
The title of the Application's window.

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

### -Width
The width of the window.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowState
The state the Application's window starts, such as Minimized.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Normal
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowStyle
The border style of the Application's window.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: SingleBorderWindow
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
