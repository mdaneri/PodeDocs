---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# Out-PodeHost

## SYNOPSIS
Outputs an object to the main Host.

## SYNTAX

```
Out-PodeHost [-InputObject] <Object> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Due to Pode's use of runspaces, this will output a given object back to the main Host.
It's advised to use this function, so that any output respects the -Quiet flag of the server.

## EXAMPLES

### EXAMPLE 1
```
'Hello, world!' | Out-PodeHost
```

### EXAMPLE 2
```
@{ Name = 'Rick' } | Out-PodeHost
```

## PARAMETERS

### -InputObject
The object to output.

```yaml
Type: Object
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
