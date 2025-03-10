---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Threading
schema: 2.0.0
---

# Lock-PodeObject

## SYNOPSIS
Places a temporary lock on an object, or Lockable, while a ScriptBlock is invoked.

## SYNTAX

### Object (Default)
```
Lock-PodeObject [[-Object] <Object>] -ScriptBlock <ScriptBlock> [-Timeout <Int32>] [-Return] [-CheckGlobal]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Name
```
Lock-PodeObject -Name <String> -ScriptBlock <ScriptBlock> [-Timeout <Int32>] [-Return] [-CheckGlobal]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Places a temporary lock on an object, or Lockable, while a ScriptBlock is invoked.

## EXAMPLES

### EXAMPLE 1
```
Lock-PodeObject -ScriptBlock { /* logic */ }
```

### EXAMPLE 2
```
Lock-PodeObject -Object $SomeArray -ScriptBlock { /* logic */ }
```

### EXAMPLE 3
```
Lock-PodeObject -Name 'LockName' -Timeout 5000 -ScriptBlock { /* logic */ }
```

### EXAMPLE 4
```
$result = (Lock-PodeObject -Return -Object $SomeArray -ScriptBlock { /* logic */ })
```

## PARAMETERS

### -CheckGlobal
If supplied, will check the global Lockable object and wait until it's freed-up before locking the passed object.

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

### -Name
The Name of a Lockable object in Pode to lock, if no Name is supplied then the global lockable is used by default.

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
The Object, or Lockable, to lock.
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
If supplied, a number of milliseconds to timeout after if a lock cannot be acquired.
(Default: Infinite)

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
