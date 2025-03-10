---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Get-PodeDefaultFolder

## SYNOPSIS
Retrieves the path of a specified default folder type from the Pode server context.

## SYNTAX

```
Get-PodeDefaultFolder [[-Type] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function returns the path for one of the Pode server's default folder types: Views, Public, or Errors.
It accesses the server's configuration stored in the \`$PodeContext\` variable and retrieves the path for the specified folder type from the \`DefaultFolders\` dictionary.
This function is useful for scripts or modules that need to dynamically access server resources based on the server's current configuration.

## EXAMPLES

### EXAMPLE 1
```
$path = Get-PodeDefaultFolder -Type 'Views'
```

This example retrieves the current path configured for the server's 'Views' folder and stores it in the \`$path\` variable.

### EXAMPLE 2
```
$path = Get-PodeDefaultFolder -Type 'Public'
```

This example retrieves the current path configured for the server's 'Public' folder.

## PARAMETERS

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
The type of the default folder for which to retrieve the path.
The valid options are 'Views', 'Public', or 'Errors'.
This parameter determines which folder's path will be returned by the function.

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

### String. The file system path of the specified default folder.
## NOTES

## RELATED LINKS
