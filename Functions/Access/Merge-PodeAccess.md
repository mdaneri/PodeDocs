---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# Merge-PodeAccess

## SYNOPSIS
Let's you merge multiple Access methods together, into a "single" Access method.

## SYNTAX

```
Merge-PodeAccess [-Name] <String> [-Access] <String[]> [[-Valid] <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Let's you merge multiple Access methods together, into a "single" Access method.
You can specify if only One or All of the methods need to pass to allow access, and you can also
merge other merged Access methods for more advanced scenarios.

## EXAMPLES

### EXAMPLE 1
```
Merge-PodeAccess -Name MergedAccess -Access RbacAccess, GbacAccess -Valid All
```

## PARAMETERS

### -Access
Mutliple Access method Names to be merged.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A unique Name for the Access method.

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

### -Valid
How many of the Access methods are required to be valid, One or All.
(Default: One)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: One
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
