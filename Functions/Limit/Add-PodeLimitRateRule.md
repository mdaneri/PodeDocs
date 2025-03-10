---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# Add-PodeLimitRateRule

## SYNOPSIS
Adds a rate limit rule.

## SYNTAX

```
Add-PodeLimitRateRule [[-Name] <String>] [[-Component] <Hashtable[]>] [[-Limit] <Int32>] [[-Duration] <Int32>]
 [[-StatusCode] <Int32>] [[-Priority] <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a rate limit rule.

## EXAMPLES

### EXAMPLE 1
```
# limit to 10 requests per minute for all IPs
Add-PodeLimitRateRule -Name 'rule1' -Limit 10 -Component @(
    New-PodeLimitIPComponent
)
```

### EXAMPLE 2
```
# limit to 5 requests per minute for all IPs and the /downloads route
Add-PodeLimitRateRule -Name 'rule1' -Limit 5 -Component @(
    New-PodeLimitIPComponent
    New-PodeLimitRouteComponent -Path '/downloads'
)
```

### EXAMPLE 3
```
# limit to 1 request, per 30 seconds, for all IPs in a subnet grouped, to the /downloads route
Add-PodeLimitRateRule -Name 'rule1' -Limit 1 -Duration 30000 -Component @(
    New-PodeLimitIPComponent -IP '10.0.0.0/24' -Group
    New-PodeLimitRouteComponent -Path '/downloads'
)
```

### EXAMPLE 4
```
# limit to 10 requests per second, for specific IPs, with a custom status code and priority
Add-PodeLimitRateRule -Name 'rule1' -Limit 10 -Duration 1000 -StatusCode 401 -Priority 100 -Component @(
    New-PodeLimitIPComponent -IP '127.0.0.1', '192.0.0.1', '10.0.0.1'
)
```

## PARAMETERS

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

### -Duration
The duration for the rule, in milliseconds.
(Default: 60000)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 60000
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit
The limit for the rule - the maximum number of requests to allow within the duration.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The name of the rate limit rule.

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
Position: 6
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
The status code to return when the limit is reached.
(Default: 429)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 429
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
