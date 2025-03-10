---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# New-PodeLimitHeaderComponent

## SYNOPSIS
Creates a new Limit Header component.

## SYNTAX

```
New-PodeLimitHeaderComponent [-Name] <String[]> [[-Value] <String[]>] [-Group]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new Limit Header component.
This support WebEvent and SmtpEvent headers.

## EXAMPLES

### EXAMPLE 1
```
New-PodeLimitHeaderComponent -Name 'X-AuthToken'
```

### EXAMPLE 2
```
New-PodeLimitHeaderComponent -Name 'X-AuthToken', 'X-AuthKey'
```

### EXAMPLE 3
```
New-PodeLimitHeaderComponent -Name 'X-AuthToken' -Value '12345'
```

### EXAMPLE 4
```
New-PodeLimitHeaderComponent -Name 'X-AuthToken' -Group
```

## PARAMETERS

### -Group
If supplied, the headers will be grouped by name, ignoring the value.
For example, any headers matching "X-AuthToken" will be grouped as "X-AuthToken", and not "X-AuthToken=123".

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

### -Name
The name of the header(s) to check.

```yaml
Type: String[]
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

### -Value
The value of the header(s) to check.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### A hashtable containing the options and scriptblock for the header component.
### The scriptblock will return the header name and value if found, or just the name if Group is supplied.
## NOTES

## RELATED LINKS
