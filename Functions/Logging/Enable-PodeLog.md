---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Enable-PodeLog

## SYNOPSIS
Enables logging in Pode.

## SYNTAX

```
Enable-PodeLog [-Terminal]
```

## DESCRIPTION
This function enables logging in Pode by setting the appropriate flags in the Pode context.

## EXAMPLES

### EXAMPLE 1
```
Enable-PodeLog
This example enables all logging except terminal logging.
```

### EXAMPLE 2
```
Enable-PodeLog -Terminal
This example enables all logging including terminal logging for the Pode C# listener.
```

## PARAMETERS

### -Terminal
A switch parameter that, if specified, enables terminal logging for the Pode C# listener.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
