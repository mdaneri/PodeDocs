---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# Add-PodeAccessCustom

## SYNOPSIS
Assigns Custom Access value(s) to a Route.

## SYNTAX

```
Add-PodeAccessCustom [-Route] <Hashtable[]> [-Name] <String> [-Value] <Object[]>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Assigns Custom Access value(s) to a Route.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeRoute -Method Get -Path '/users' -ScriptBlock {} -PassThru | Add-PodeAccessCustom -Name 'Example' -Value @{ Country = 'UK' }
```

## PARAMETERS

### -Name
The Name of the Access method the Custom Access value(s) are for.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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

### -Route
The Route to assign the Custom Access value(s).

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Value
The Custom Access Value(s)

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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
