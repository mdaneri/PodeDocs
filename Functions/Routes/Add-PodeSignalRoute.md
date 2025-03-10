---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Routes
schema: 2.0.0
---

# Add-PodeSignalRoute

## SYNOPSIS
Adds a Signal Route for WebSockets.

## SYNTAX

### Script (Default)
```
Add-PodeSignalRoute -Path <String> [-ScriptBlock <ScriptBlock>] [-EndpointName <String[]>]
 [-ArgumentList <Object[]>] [-IfExists <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodeSignalRoute -Path <String> [-EndpointName <String[]>] -FilePath <String> [-ArgumentList <Object[]>]
 [-IfExists <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a Signal Route, with path, that when called with invoke any logic.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeSignalRoute -Path '/message' -ScriptBlock { /* logic */ }
```

### EXAMPLE 2
```
Add-PodeSignalRoute -Path '/message' -ScriptBlock { /* logic */ } -ArgumentList 'arg1', 'arg2'
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Signal Route's ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
The EndpointName of an Endpoint(s) this Signal Route should be bound against.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the Signal Route's main logic.

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

### -IfExists
Specifies what action to take when a Signal Route already exists.
(Default: Default)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The URI path for the Signal Route.

```yaml
Type: String
Parameter Sets: (All)
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

### -ScriptBlock
A ScriptBlock for the Signal Route's main logic.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

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

### System.Object[]
## NOTES

## RELATED LINKS
