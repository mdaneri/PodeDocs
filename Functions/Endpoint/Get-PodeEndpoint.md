---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Endpoint
schema: 2.0.0
---

# Get-PodeEndpoint

## SYNOPSIS
Get an Endpoint(s).

## SYNTAX

```
Get-PodeEndpoint [[-Address] <String>] [[-Port] <Int32>] [[-Hostname] <String>] [[-Protocol] <String>]
 [[-Name] <String[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Get an Endpoint(s).

## EXAMPLES

### EXAMPLE 1
```
Get-PodeEndpoint -Address 127.0.0.1
```

### EXAMPLE 2
```
Get-PodeEndpoint -Protocol Http
```

### EXAMPLE 3
```
Get-PodeEndpoint -Name Admin, User
```

## PARAMETERS

### -Address
An Address to filter the endpoints.

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

### -Hostname
A Hostname to filter the endpoints.

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

### -Name
Any endpoints Names to filter endpoints.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
A Port to filter the endpoints.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### -Protocol
A Protocol to filter the endpoints.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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
