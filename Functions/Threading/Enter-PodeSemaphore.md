---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Threading
schema: 2.0.0
---

# Enter-PodeSemaphore

## SYNOPSIS
Acquires a hold on a Semaphore.

## SYNTAX

```
Enter-PodeSemaphore [-Name] <String> [[-Timeout] <Int32>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Acquires a hold on a Semaphore.
This should eventually by followed by a call to Exit-PodeSemaphore.

## EXAMPLES

### EXAMPLE 1
```
Enter-PodeSemaphore -Name 'SelfSemaphore' -Timeout 5000
```

## PARAMETERS

### -Name
The Name of the Semaphore.

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

### -Timeout
If supplied, a number of milliseconds to timeout after if a hold cannot be acquired on the Semaphore.
(Default: Infinite)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
