---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Threading
schema: 2.0.0
---

# Use-PodeMutex

## SYNOPSIS
Places a temporary hold on a Mutex, invokes a ScriptBlock, then releases the Mutex.

## SYNTAX

```
Use-PodeMutex [-Name] <String> [-ScriptBlock] <ScriptBlock> [[-Timeout] <Int32>] [-Return]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Places a temporary hold on a Mutex, invokes a ScriptBlock, then releases the Mutex.

## EXAMPLES

### EXAMPLE 1
```
Use-PodeMutex -Name 'SelfMutex' -Timeout 5000 -ScriptBlock {}
```

### EXAMPLE 2
```
$result = Use-PodeMutex -Name 'LocalMutex' -Return -ScriptBlock {}
```

## PARAMETERS

### -Name
The Name of the Mutex.

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

### -Return
If supplied, any values from the ScriptBlock will be returned.

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

### -ScriptBlock
The ScriptBlock to invoke.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
If supplied, a number of milliseconds to timeout after if a hold cannot be acquired on the Mutex.
(Default: Infinite)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
