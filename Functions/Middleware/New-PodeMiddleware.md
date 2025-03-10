---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Middleware
schema: 2.0.0
---

# New-PodeMiddleware

## SYNOPSIS
Creates a new Middleware HashTable object, that can be piped/used in Add-PodeMiddleware or in Routes.

## SYNTAX

```
New-PodeMiddleware [-ScriptBlock] <ScriptBlock> [-Route <String>] [-ArgumentList <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new Middleware HashTable object, that can be piped/used in Add-PodeMiddleware or in Routes.
ScriptBlock should return $true to continue execution, or $false to stop.

## EXAMPLES

### EXAMPLE 1
```
New-PodeMiddleware -ScriptBlock { /* logic */ } -ArgumentList 'Email' | Add-PodeMiddleware -Name 'CheckEmail'
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Middleware's ScriptBlock.

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

### -Route
A Route path for which Routes this Middleware should only be invoked against.

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

### -ScriptBlock
The Script that defines the logic of the Middleware.
Should return $true to continue execution, or $false to stop.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Boolean. ScriptBlock should return $true to continue to the next middleware/route, or return $false to stop execution.
## NOTES

## RELATED LINKS
