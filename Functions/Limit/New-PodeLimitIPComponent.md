---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Limit
schema: 2.0.0
---

# New-PodeLimitIPComponent

## SYNOPSIS
Creates a new Limit IP component.

## SYNTAX

```
New-PodeLimitIPComponent [[-IP] <String[]>] [[-Location] <String>] [[-XForwardedForType] <String>] [-Group]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Creates a new Limit IP component.
This supports the WebEvent, SmtpEvent, and TcpEvent IPs.

## EXAMPLES

### EXAMPLE 1
```
New-PodeLimitIPComponent
```

### EXAMPLE 2
```
New-PodeLimitIPComponent -IP '127.0.0.1'
```

### EXAMPLE 3
```
New-PodeLimitIPComponent -IP '10.0.0.0/24'
```

### EXAMPLE 4
```
New-PodeLimitIPComponent -IP 'localhost'
```

### EXAMPLE 5
```
New-PodeLimitIPComponent -IP 'all'
```

### EXAMPLE 6
```
New-PodeLimitIPComponent -IP '192.0.1.0/16' -Group
```

### EXAMPLE 7
```
New-PodeLimitIPComponent -IP '10.0.0.1' -Location XForwardedFor
```

### EXAMPLE 8
```
New-PodeLimitIPComponent -IP '192.0.1.0/16' -Group -Location XForwardedFor -XForwardedForType Rightmost
```

## PARAMETERS

### -Group
If supplied, IPs in a subnet will be treated as a single entity.

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

### -IP
The IP address(es) to check.
Supports raw IPs, subnets, local, and any.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Where to get the IP from: RemoteAddress or XForwardedFor.
(Default: RemoteAddress)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: RemoteAddress
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

### -XForwardedForType
If the Location is XForwardedFor, which IP in the X-Forwarded-For header to use: Leftmost, Rightmost, or All.
(Default: Leftmost)
If Leftmost, the first IP in the X-Forwarded-For header will be used.
If Rightmost, the last IP in the X-Forwarded-For header will be used.
If All, all IPs in the X-Forwarded-For header will be used - at least one must match.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Leftmost
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### A hashtable containing the options and scriptblock for the IP component.
### The scriptblock will return the IP - or subnet for grouped - if found, or null if not.
## NOTES

## RELATED LINKS
