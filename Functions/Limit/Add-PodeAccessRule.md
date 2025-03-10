---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# Add-PodeAccessRule

## SYNOPSIS
Adds an access rule to allow or deny IP addresses.
This is a legacy function, use Add-PodeLimitAccessRule instead.

## SYNTAX

```
Add-PodeAccessRule [-Access] <String> [-Type] <String> [-Values] <String[]>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds an access rule to allow or deny IP addresses.
This is a legacy function, use Add-PodeLimitAccessRule instead.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeAccessRule -Access Allow -Type IP -Values '127.0.0.1'
```

### EXAMPLE 2
```
Add-PodeAccessRule -Access Deny -Type IP -Values @('192.168.1.1', '10.10.1.0/24')
```

## PARAMETERS

### -Access
The type of access to enable.

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

### -Type
What type of request are we configuring?

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

### -Values
A single, or an array of values.

```yaml
Type: String[]
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
