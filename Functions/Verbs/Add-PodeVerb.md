---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Verbs
schema: 2.0.0
---

# Add-PodeVerb

## SYNOPSIS
Adds a Verb for a TCP data.

## SYNTAX

### Script (Default)
```
Add-PodeVerb -Verb <String> [-ScriptBlock <ScriptBlock>] [-ArgumentList <Object[]>] [-EndpointName <String[]>]
 [-UpgradeToSsl] [-Close] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### File
```
Add-PodeVerb -Verb <String> -FilePath <String> [-ArgumentList <Object[]>] [-EndpointName <String[]>]
 [-UpgradeToSsl] [-Close] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds a Verb for a TCP data.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeVerb -Verb 'Hello' -ScriptBlock { /* logic */ }
```

### EXAMPLE 2
```
Add-PodeVerb -Verb 'Hello' -ScriptBlock { /* logic */ } -ArgumentList 'arg1', 'arg2'
```

### EXAMPLE 3
```
Add-PodeVerb -Verb 'Quit' -Close
```

### EXAMPLE 4
```
Add-PodeVerb -Verb 'StartTls' -UpgradeToSsl
```

## PARAMETERS

### -ArgumentList
An array of arguments to supply to the Verb's ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Close
If supplied, the Verb will auto-close the connection.

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

### -EndpointName
The EndpointName of an Endpoint(s) this Verb should be bound against.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
A literal, or relative, path to a file containing a ScriptBlock for the Verb's main logic.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: True
Position: Named
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

### -ScriptBlock
A ScriptBlock for the Verb's main logic.

```yaml
Type: ScriptBlock
Parameter Sets: Script
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeToSsl
If supplied, the Verb will auto-upgrade the connection to use SSL.

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

### -Verb
The Verb for the Verb.

```yaml
Type: String
Parameter Sets: (All)
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
