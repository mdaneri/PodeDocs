---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# New-PodeLimitRouteComponent

## SYNOPSIS
Creates a new Limit Route component.

## SYNTAX

```
New-PodeLimitRouteComponent [[-Path] <String[]>] [-Group] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Creates a new Limit Route component.
This supports the WebEvent routes.

## EXAMPLES

### EXAMPLE 1
```
New-PodeLimitRouteComponent -Path '/downloads'
```

### EXAMPLE 2
```
New-PodeLimitRouteComponent -Path '/downloads', '/api/*'
```

### EXAMPLE 3
```
New-PodeLimitRouteComponent -Path '/api/*' -Group
```

## PARAMETERS

### -Group
If supplied, the routes will be grouped by any wildcard, ignoring the full path.
For example, any routes matching "/api/*" will be grouped as "/api/*", and not "/api/test" or "/api/test/hello".

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
The route path(s) to check.
This can be a full path, or a wildcard path.

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

### A hashtable containing the options and scriptblock for the route component.
### The scriptblock will return the route path if found, or null if not.
## NOTES

## RELATED LINKS
