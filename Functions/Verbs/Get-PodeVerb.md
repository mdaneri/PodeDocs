---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Verbs
schema: 2.0.0
---

# Get-PodeVerb

## SYNOPSIS
Get a Verb(s).

## SYNTAX

```
Get-PodeVerb [[-Verb] <String>] [[-EndpointName] <String[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Get a Verb(s).

## EXAMPLES

### EXAMPLE 1
```
Get-PodeVerb -Verb 'Hello'
```

### EXAMPLE 2
```
Get-PodeVerb -Verb 'Hello :username' -EndpointName User
```

## PARAMETERS

### -EndpointName
The name of an endpoint to filter verbs.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -Verb
A Verb to filter the verbs.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
