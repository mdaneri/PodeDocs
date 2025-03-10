---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Security
schema: 2.0.0
---

# Set-PodeSecurityContentSecurityPolicy

## SYNOPSIS
Set the value to use for the Content-Security-Policy and X-XSS-Protection headers.

## SYNTAX

```
Set-PodeSecurityContentSecurityPolicy [[-Default] <String[]>] [[-Child] <String[]>] [[-Connect] <String[]>]
 [[-Font] <String[]>] [[-Frame] <String[]>] [[-Image] <String[]>] [[-Manifest] <String[]>]
 [[-Media] <String[]>] [[-Object] <String[]>] [[-Scripts] <String[]>] [[-Style] <String[]>]
 [[-BaseUri] <String[]>] [[-FormAction] <String[]>] [[-FrameAncestor] <String[]>] [[-FencedFrame] <String[]>]
 [[-Prefetch] <String[]>] [[-ScriptAttr] <String[]>] [[-ScriptElem] <String[]>] [[-StyleAttr] <String[]>]
 [[-StyleElem] <String[]>] [[-Worker] <String[]>] [[-Sandbox] <String>] [[-ReportUri] <String>]
 [-UpgradeInsecureRequests] [-XssBlock] [-ReportOnly] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Set the value to use for the Content-Security-Policy and X-XSS-Protection headers.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeSecurityContentSecurityPolicy -Default 'self'
```

## PARAMETERS

### -BaseUri
The values to use for the BaseUri portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Child
The values to use for the Child portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Connect
The values to use for the Connect portion of the header.

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

### -Default
The values to use for the Default portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FencedFrame
The values to use for the FencedFrame portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Font
The values to use for the Font portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FormAction
The values to use for the FormAction portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frame
The values to use for the Frame portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrameAncestor
The values to use for the FrameAncestor portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Image
The values to use for the Image portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Manifest
The values to use for the Manifest portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Media
The values to use for the Media portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Object
The values to use for the Object portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefetch
The values to use for the Prefetch portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 16
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

### -ReportOnly
If supplied, the header will be set as a report-only header.

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

### -ReportUri
The value to use for the ReportUri portion of the header.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 23
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sandbox
The value to use for the Sandbox portion of the header.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptAttr
The values to use for the ScriptAttr portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptElem
The values to use for the ScriptElem portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 18
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scripts
The values to use for the Scripts portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Style
The values to use for the Style portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StyleAttr
The values to use for the StyleAttr portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 19
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StyleElem
The values to use for the StyleElem portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 20
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeInsecureRequests
If supplied, the header will have the upgrade-insecure-requests value added.

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

### -Worker
The values to use for the Worker portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XssBlock
If supplied, the X-XSS-Protection header will be set to blocking mode.
(Default: Off)

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
