---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Set-PodeDefaultFolder

## SYNOPSIS
Sets the path for a specified default folder type in the Pode server context.

## SYNTAX

```
Set-PodeDefaultFolder [[-Type] <String>] [[-Path] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This function configures the path for one of the Pode server's default folder types: Views, Public, or Errors.
It updates the server's configuration to reflect the new path for the specified folder type.
The function first checks if the provided path exists and is a directory;
if so, it updates the \`Server.DefaultFolders\` dictionary with the new path.
If the path does not exist or is not a directory, the function throws an error.

The purpose of this function is to allow dynamic configuration of the server's folder paths, which can be useful during server setup or when altering the server's directory structure at runtime.

## EXAMPLES

### EXAMPLE 1
```
Set-PodeDefaultFolder -Type 'Views' -Path 'C:\Pode\Views'
```

This example sets the path for the server's default 'Views' folder to 'C:\Pode\Views', assuming this path exists and is a directory.

### EXAMPLE 2
```
Set-PodeDefaultFolder -Type 'Public' -Path 'C:\Pode\Public'
```

This example sets the path for the server's default 'Public' folder to 'C:\Pode\Public'.

## PARAMETERS

### -Path
The new file system path for the specified default folder type.
This path must exist and be a directory; otherwise, an exception is thrown.

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

### -Type
The type of the default folder to set the path for.
Must be one of 'Views', 'Public', or 'Errors'.
This parameter determines which default folder's path is being set.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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
