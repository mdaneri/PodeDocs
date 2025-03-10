---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# Update-PodeLimitAccessRule

## SYNOPSIS
Updates an access rule.

## SYNTAX

```
Update-PodeLimitAccessRule [-Name] <String> [[-Action] <String>] [[-StatusCode] <Int32>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Updates an access rule.

## EXAMPLES

### EXAMPLE 1
```
Update-PodeLimitAccessRule -Name 'rule1' -Action 'Deny'
```

### EXAMPLE 2
```
Update-PodeLimitAccessRule -Name 'rule1' -StatusCode 404
```

### EXAMPLE 3
```
Update-PodeLimitAccessRule -Name 'rule1' -Action 'Allow' -StatusCode 200
```

## PARAMETERS

### -Action
The action to take.
Either 'Allow' or 'Deny'.
If not supplied, the action will not be updated.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the access rule.

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

### -StatusCode
The status code to return.
If not supplied, the status code will not be updated.

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
