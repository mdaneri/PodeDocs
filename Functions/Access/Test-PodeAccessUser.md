---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# Test-PodeAccessUser

## SYNOPSIS
Test the currently authenticated User's access against the supplied values.

## SYNTAX

```
Test-PodeAccessUser [-Name] <String> [-Value] <Object[]> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Test the currently authenticated User's access against the supplied values.
This will be the user in a WebEvent object.

## EXAMPLES

### EXAMPLE 1
```
if (Test-PodeAccessUser -Name 'Example' -Value 'Developer', 'QA') { }
```

## PARAMETERS

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

### -Value
An array of access values to pass to the Access method for verification against the User.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
