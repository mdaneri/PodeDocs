---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Test-PodeRequestFile

## SYNOPSIS
Test to see if the Request contains the key for any uploaded files.

## SYNTAX

```
Test-PodeRequestFile [-Key] <String> [[-FileName] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Test to see if the Request contains the key for any uploaded files.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeRequestFile -Key 'avatar'
```

### EXAMPLE 2
```
Test-PodeRequestFile -Key 'avatar' -FileName 'icon.png'
```

## PARAMETERS

### -FileName
An optional FileName to test for a specific file within the list of uploaded files.

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

### System.Boolean
## NOTES

## RELATED LINKS
