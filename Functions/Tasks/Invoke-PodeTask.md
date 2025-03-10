---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Tasks
schema: 2.0.0
---

# Invoke-PodeTask

## SYNOPSIS
Invoke a Task.

## SYNTAX

```
Invoke-PodeTask [-Name] <String> [-ArgumentList <Hashtable>] [-Timeout <Int32>] [-TimeoutFrom <String>] [-Wait]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Invoke a Task either asynchronously or synchronously, with support for returning values.
The function returns the Task process object which was triggered.

## EXAMPLES

### EXAMPLE 1
```
Invoke-PodeTask -Name 'Example1' -Wait -Timeout 5
```

### EXAMPLE 2
```
$task = Invoke-PodeTask -Name 'Example1'
```

### EXAMPLE 3
```
Invoke-PodeTask -Name 'Example1' | Wait-PodeTask -Timeout 3
```

## PARAMETERS

### -ArgumentList
A hashtable of arguments to supply to the Task's ScriptBlock.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Task.

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

### -Timeout
A Timeout, in seconds, to abort running the Task process.
(Default: -1 \[never timeout\])

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeoutFrom
Where to start the Timeout from, either 'Default', 'Create', or 'Start'.
(Default: 'Default' - will use the value from Add-PodeTask)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wait
If supplied, Pode will wait until the Task process has finished executing, and then return any values.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### The triggered Task process.
## NOTES

## RELATED LINKS
