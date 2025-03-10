---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Logging
schema: 2.0.0
---

# Disable-PodeLog

## SYNOPSIS
Disables logging in Pode.

## SYNTAX

```
Disable-PodeLog [-KeepTerminal]
```

## DESCRIPTION
This function disables logging in Pode by setting the appropriate flags in the Pode context.
It allows you to optionally keep terminal logging enabled.

## EXAMPLES

### EXAMPLE 1
```
Disable-PodeLog
This example disables all logging including terminal logging.
```

### EXAMPLE 2
```
Disable-PodeLog -KeepTerminal
This example disables all logging except terminal logging.
```

## PARAMETERS

### -KeepTerminal
A switch parameter that, if specified, keeps terminal logging enabled for the Pode C# listener even when other logging is disabled.

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
