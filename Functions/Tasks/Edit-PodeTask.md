---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Tasks
schema: 2.0.0
---

# Edit-PodeTask

## SYNOPSIS
Edits an existing Task.

## SYNTAX

```
Edit-PodeTask [-Name] <String> [-ScriptBlock <ScriptBlock>] [-ArgumentList <Hashtable>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Edits an existing Task's properties, such as scriptblock.

## EXAMPLES

### EXAMPLE 1
```
Edit-PodeTask -Name 'Example1' -ScriptBlock { Invoke-SomeNewLogic }
```

## PARAMETERS

### -ArgumentList
Any new Arguments for the Task.

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

### -ScriptBlock
The new ScriptBlock for the Task.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

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
