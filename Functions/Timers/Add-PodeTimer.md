---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Timers
schema: 2.0.0
---

# Add-PodeTimer

## SYNOPSIS
Adds a new Timer with logic to periodically invoke.

## SYNTAX

### Script (Default)
```
Add-PodeTimer -Name <String> -Interval <Int32> -ScriptBlock <ScriptBlock> [-Limit <Int32>] [-Skip <Int32>]
 [-ArgumentList <Object[]>] [-OnStart] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodeTimer -Name <String> -Interval <Int32> [-Limit <Int32>] [-Skip <Int32>] -FilePath <String>
 [-ArgumentList <Object[]>] [-OnStart] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a new Timer with logic to periodically invoke, with options to only run a specific number of times.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeTimer -Name 'Hello' -Interval 10 -ScriptBlock { 'Hello, world!' | Out-Default }
```

### EXAMPLE 2
```
Add-PodeTimer -Name 'RunOnce' -Interval 1 -Limit 1 -ScriptBlock { /* logic */ }
```

### EXAMPLE 3
```
Add-PodeTimer -Name 'RunAfter60secs' -Interval 10 -Skip 6 -ScriptBlock { /* logic */ }
```

### EXAMPLE 4
```
Add-PodeTimer -Name 'Args' -Interval 2 -ScriptBlock { /* logic */ } -ArgumentList 'arg1', 'arg2'
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Timer's ScriptBlock.

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

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the Timer's logic.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Interval
The number of seconds to periodically invoke the Timer's ScriptBlock.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit
The number of times the Timer should be invoked before being removed.
(If 0, it will run indefinitely)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Timer.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnStart
If supplied, the timer will trigger when the server starts.

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

### -ScriptBlock
The script for the Timer.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
The number of "invokes" to skip before the Timer actually runs.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
