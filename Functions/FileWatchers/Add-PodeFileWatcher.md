---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: FileWatchers
schema: 2.0.0
---

# Add-PodeFileWatcher

## SYNOPSIS
Adds a new File Watcher to monitor file changes in a directory.

## SYNTAX

### Script (Default)
```
Add-PodeFileWatcher [-Name <String>] [-EventName <String[]>] -Path <String> -ScriptBlock <ScriptBlock>
 [-ArgumentList <Object[]>] [-NotifyFilter <NotifyFilters[]>] [-Exclude <String[]>] [-Include <String[]>]
 [-InternalBufferSize <Int32>] [-NoSubdirectories] [-PassThru] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### File
```
Add-PodeFileWatcher [-Name <String>] [-EventName <String[]>] -Path <String> -FilePath <String>
 [-ArgumentList <Object[]>] [-NotifyFilter <NotifyFilters[]>] [-Exclude <String[]>] [-Include <String[]>]
 [-InternalBufferSize <Int32>] [-NoSubdirectories] [-PassThru] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Adds a new File Watcher to monitor file changes in a directory.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeFileWatcher -Path 'C:/Projects/:project/src' -Include '*.ps1' -ScriptBlock {}
```

### EXAMPLE 2
```
Add-PodeFileWatcher -Path 'C:/Websites/:site' -Include '*.config' -EventName Changed -ScriptBlock {}
```

### EXAMPLE 3
```
Add-PodeFileWatcher -Path '/temp/logs' -EventName Created -NotifyFilter CreationTime -ScriptBlock {}
```

### EXAMPLE 4
```
$watcher = Add-PodeFileWatcher -Path '/temp/logs' -Exclude *.txt -ScriptBlock {} -PassThru
```

## PARAMETERS

### -ArgumentList
A hashtable of arguments to supply to the File Watcher's ScriptBlock.

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

### -EventName
An optional EventName to be monitored.
Note: '*' refers to all event names.
(Default: Changed, Created, Deleted, Renamed)

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: @('Changed', 'Created', 'Deleted', 'Renamed')
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exclude
An optional array of file patterns to be excluded.

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
A literal, or relative, path to a file containing a ScriptBlock for the File Watcher's logic.

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

### -Include
An optional array of file patterns to be included.
(Default: *.*)

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: *.*
Accept pipeline input: False
Accept wildcard characters: False
```

### -InternalBufferSize
The InternalBufferSize of the file monitor, used when temporarily storing events.
(Default: 8kb)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 8192
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
An optional Name for the File Watcher.
(Default: GUID)

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

### -NoSubdirectories
If supplied, the File Watcher will only monitor files in the specified directory path, and not in all sub-directories as well.

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

### -NotifyFilter
The attributes on files to monitor and notify about.
(Default: FileName, DirectoryName, LastWrite, CreationTime)

```yaml
Type: NotifyFilters[]
Parameter Sets: (All)
Aliases:
Accepted values: FileName, DirectoryName, Attributes, Size, LastWrite, LastAccess, CreationTime, Security

Required: False
Position: Named
Default value: @('FileName', 'DirectoryName', 'LastWrite', 'CreationTime')
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
If supplied, the File Watcher object registered will be returned.

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
The Path to a directory which contains the files to be monitored.

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
The ScriptBlock defining logic to be run when events are triggered.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: True
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
