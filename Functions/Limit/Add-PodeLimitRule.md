---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# Add-PodeLimitRule

## SYNOPSIS
Adds rate limiting rules for an IP addresses, Routes, or Endpoints.
This is a legacy function, use Add-PodeLimitRateRule instead.

## SYNTAX

```
Add-PodeLimitRule [-Type] <String> [-Values] <String[]> [-Limit] <Int32> [-Seconds] <Int32> [-Group]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds rate limiting rules for an IP addresses, Routes, or Endpoints.
This is a legacy function, use Add-PodeLimitRateRule instead.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeLimitRule -Type IP -Values '127.0.0.1' -Limit 10 -Seconds 1
```

### EXAMPLE 2
```
Add-PodeLimitRule -Type IP -Values @('192.168.1.1', '10.10.1.0/24') -Limit 50 -Seconds 1 -Group
```

### EXAMPLE 3
```
Add-PodeLimitRule -Type Route -Values '/downloads' -Limit 5 -Seconds 1
```

## PARAMETERS

### -Group
If supplied, groups of IPs in a subnet will be considered as one IP.

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

### -Limit
The maximum number of requests to allow.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: 0
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

### -Seconds
The number of seconds to count requests before restarting the count.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
What type of request is being rate limited: IP, Route, or Endpoint?

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

### -Values
A single, or an array of values.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
