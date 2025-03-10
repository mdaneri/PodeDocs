---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Threading
schema: 2.0.0
---

# Exit-PodeLockable

## SYNOPSIS
Remove a lock from an object or Lockable.

## SYNTAX

### Object (Default)
```
Exit-PodeLockable [[-Object] <Object>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Name
```
Exit-PodeLockable -Name <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Remove a lock from an object or Lockable, that was originally locked via Enter-PodeLockable.

## EXAMPLES

### EXAMPLE 1
```
Exit-PodeLockable -Object $SomeArray
```

### EXAMPLE 2
```
Exit-PodeLockable -Name 'LockName'
```

## PARAMETERS

### -Name
The Name of a Lockable object in Pode to unlock, if no Name is supplied then the global lockable is used by default.

```yaml
Type: String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Object
The Object, or Lockable, to unlock.
If no Object is supplied then the global lockable is used by default.

```yaml
Type: Object
Parameter Sets: Object
Aliases:

Required: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
