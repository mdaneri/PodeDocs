---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Move-PodeResponseUrl

## SYNOPSIS
Redirecting a user to a new URL.

## SYNTAX

### Url (Default)
```
Move-PodeResponseUrl -Url <String> [-Moved] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Endpoint
```
Move-PodeResponseUrl [-EndpointName <String>] [-Moved] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### Components
```
Move-PodeResponseUrl [-Port <Int32>] [-Protocol <String>] [-Address <String>] [-Moved]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Redirecting a user to a new URL, or the same URL as the Request but a different Protocol - or other components.

## EXAMPLES

### EXAMPLE 1
```
Move-PodeResponseUrl -Url 'https://google.com'
```

### EXAMPLE 2
```
Move-PodeResponseUrl -Url '/about'
```

### EXAMPLE 3
```
Move-PodeResponseUrl -Protocol HTTPS
```

### EXAMPLE 4
```
Move-PodeResponseUrl -Port 9000 -Moved
```

## PARAMETERS

### -Address
Change the domain address of the current Request before redirecting.

```yaml
Type: String
Parameter Sets: Components
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
The Name of an Endpoint to redirect to.

```yaml
Type: String
Parameter Sets: Endpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Moved
Set the Status Code as "301 Moved", rather than "302 Redirect".

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

### -Port
Change the port of the current Request before redirecting.

```yaml
Type: Int32
Parameter Sets: Components
Aliases:

Required: False
Position: Named
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
Change the protocol of the current Request before redirecting.

```yaml
Type: String
Parameter Sets: Components
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url
Redirect the user to a new URL, or a relative path.

```yaml
Type: String
Parameter Sets: Url
Aliases:

Required: True
Position: Named
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
