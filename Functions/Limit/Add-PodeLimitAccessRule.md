---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# Add-PodeLimitAccessRule

## SYNOPSIS
Adds an access limit rule.

## SYNTAX

```
Add-PodeLimitAccessRule [[-Name] <String>] [[-Component] <Hashtable[]>] [[-Action] <String>]
 [[-StatusCode] <Int32>] [[-Priority] <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds an access limit rule.

## EXAMPLES

### EXAMPLE 1
```
# only allow localhost
Add-PodeLimitAccessRule -Name 'rule1' -Action Allow -Component @(
    New-PodeLimitIPComponent -IP '127.0.0.1'
)
```

### EXAMPLE 2
```
# only allow localhost and the /downloads route
Add-PodeLimitAccessRule -Name 'rule1' -Action Allow -Component @(
    New-PodeLimitIPComponent -IP '127.0.0.1'
    New-PodeLimitRouteComponent -Path '/downloads'
)
```

### EXAMPLE 3
```
# deny all requests
Add-PodeLimitAccessRule -Name 'rule1' -Action Deny -Component @(
    New-PodeLimitIPComponent
)
```

### EXAMPLE 4
```
# deny all requests from a subnet, with a custom status code
Add-PodeLimitAccessRule -Name 'rule1' -Action Deny -StatusCode 401 -Component @(
    New-PodeLimitIPComponent -IP '10.0.0.0/24'
)
```

### EXAMPLE 5
```
# deny all requests from a subnet, with a custom status code and priority
Add-PodeLimitAccessRule -Name 'rule1' -Action Deny -StatusCode 401 -Priority 100 -Component @(
    New-PodeLimitIPComponent -IP '192.0.1.0/16'
)
```

## PARAMETERS

### -Action
The action to take.
Either 'Allow' or 'Deny'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Component
The component(s) to check.
This can be a single, or an array of components.

```yaml
Type: Hashtable[]
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

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
The priority of the rule.
The higher the number, the higher the priority.
(Default: \[int\]::MinValue)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -2147483648
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
(Default: 403)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 403
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
