---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# Test-PodeAccess

## SYNOPSIS
Test access values for a Source/Destination against an Access method.

## SYNTAX

```
Test-PodeAccess [-Name] <String> [[-Source] <Object[]>] [[-Destination] <Object[]>]
 [[-ArgumentList] <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Test access values for a Source/Destination against an Access method.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeAccess -Name 'Example' -Source 'Developer' -Destination 'Admin') { }
```

## PARAMETERS

### -ArgumentList
An optional array of arguments to supply to the Access Scheme's ScriptBlock for retrieving access values.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destination
An array of Destination access values to pass to the Access method for verification.
(ie: Route)

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Access method to use to verify the access.

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

### -Source
An array of Source access values to pass to the Access method for verification against the Destination access values.
(ie: User)

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Boolean
## NOTES

## RELATED LINKS
