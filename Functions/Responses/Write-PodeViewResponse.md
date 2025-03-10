---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Write-PodeViewResponse

## SYNOPSIS
Renders a dynamic, or static, View on the Response.

## SYNTAX

```
Write-PodeViewResponse [-Path] <String> [-Data <Hashtable>] [-StatusCode <Int32>] [-Folder <String>]
 [-FlashMessages] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Renders a dynamic, or static, View on the Response; allowing for dynamic data to be supplied.

## EXAMPLES

### EXAMPLE 1
```
Write-PodeViewResponse -Path 'index'
```

### EXAMPLE 2
```
Write-PodeViewResponse -Path 'accounts/profile_page' -Data @{ Username = 'Morty' }
```

### EXAMPLE 3
```
Write-PodeViewResponse -Path 'login' -FlashMessages
```

## PARAMETERS

### -Data
Any dynamic data to supply to a dynamic View.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: @{}
Accept pipeline input: False
Accept wildcard characters: False
```

### -FlashMessages
Automatically supply all Flash messages in the current session to the View.

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

### -Folder
If supplied, a custom views folder will be used.

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

### -Path
The path to a View, relative to the "/views" directory.
(Extension is optional).

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
