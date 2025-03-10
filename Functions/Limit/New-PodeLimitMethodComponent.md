---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# New-PodeLimitMethodComponent

## SYNOPSIS
Creates a new Limit HTTP Method component.

## SYNTAX

```
New-PodeLimitMethodComponent [[-Method] <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new Limit HTTP Method component.
This supports the WebEvent methods.

## EXAMPLES

### EXAMPLE 1
```
New-PodeLimitMethodComponent
```

### EXAMPLE 2
```
New-PodeLimitMethodComponent -Method 'Get'
```

### EXAMPLE 3
```
New-PodeLimitMethodComponent -Method 'Get', 'Post'
```

## PARAMETERS

### -Method
The HTTP method(s) to check.

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

### A hashtable containing the options and scriptblock for the method component.
### The scriptblock will return the method if found, or null if not.
## NOTES

## RELATED LINKS
