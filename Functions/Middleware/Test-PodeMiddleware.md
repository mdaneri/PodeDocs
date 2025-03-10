---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Middleware
schema: 2.0.0
---

# Test-PodeMiddleware

## SYNOPSIS
Checks if a specific middleware is registered in the Pode server.

## SYNTAX

```
Test-PodeMiddleware [-Name] <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function verifies whether a middleware with the specified name is registered in the Pode server by checking the \`PodeContext.Server.Middleware\` collection.
It returns \`$true\` if the middleware exists, otherwise it returns \`$false\`.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeMiddleware -Name 'BlockEverything'
```

This command checks if a middleware named 'BlockEverything' is registered in the Pode server.

## PARAMETERS

### -Name
The name of the middleware to check for.

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

### [boolean]
###     Returns $true if the middleware with the specified name is found, otherwise returns $false.
## NOTES

## RELATED LINKS
