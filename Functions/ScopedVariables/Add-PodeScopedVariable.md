---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: ScopedVariables
schema: 2.0.0
---

# Add-PodeScopedVariable

## SYNOPSIS
Adds a new Scoped Variable.

## SYNTAX

### Replace (Default)
```
Add-PodeScopedVariable -Name <String> -GetReplace <String> [-SetReplace <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ScriptBlock
```
Add-PodeScopedVariable -Name <String> -ScriptBlock <ScriptBlock> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Adds a new Scoped Variable, to make calling certain functions simpler.
For example "$state:Name" instead of "Get-PodeState" and "Set-PodeState".

## EXAMPLES

### EXAMPLE 1
```
Add-PodeScopedVariable -Name 'cache' -SetReplace "Set-PodeCache -Key '{{name}}' -InputObject " -GetReplace "Get-PodeCache -Key '{{name}}'"
```

### EXAMPLE 2
```
Add-PodeScopedVariable -Name 'config' -ScriptBlock {
    param($ScriptBlock, $SessionState, $GetPattern, $SetPattern)
    $strScriptBlock = "$($ScriptBlock)"
    $template = "(Get-PodeConfig).'{{name}}'"
```

# allows "$port = $config:port" instead of "$port = (Get-PodeConfig).port"
    while ($strScriptBlock -imatch $GetPattern) {
        $getReplace = $template.Replace('{{name}}', $Matches\['name'\])
        $strScriptBlock = $strScriptBlock.Replace($Matches\['full'\], "($($getReplace))")
    }

    return \[scriptblock\]::Create($strScriptBlock)
}

## PARAMETERS

### -GetReplace
A template to be used when converting "$var = $SV:\<name\>" to a "Get-SVValue -Name \<name\>" syntax.
You can use the "{{name}}" placeholder to show where the \<name\> would be placed in the conversion.
The result will also be automatically wrapped in brackets.
For example, "$var = $state:\<name\>" to "Get-PodeState -Name \<name\>" would need a GetReplace value of "Get-PodeState -Name '{{name}}'".

```yaml
Type: String
Parameter Sets: Replace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The Name of the Scoped Variable.

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
For more advanced conversions, that aren't as simple as a simple find/replace, you can supply a ScriptBlock instead.
This ScriptBlock will be supplied ScriptBlock to convert, followed by a SessionState object, and the Get/Set regex patterns, as parameters.
The ScriptBlock should returned a converted ScriptBlock that works, plus an optional array of values that should be supplied to the ScriptBlock when invoked.

```yaml
Type: ScriptBlock
Parameter Sets: ScriptBlock
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetReplace
An optional template to be used when converting "$SV:\<name\> = \<value\>" to a "Set-SVValue -Name \<name\> -Value \<value\>" syntax.
You can use the "{{name}}" placeholder to show where the \<name\> would be placed in the conversion.
The \<value\> will automatically be appended to the end.
For example, "$state:\<name\> = \<value\>" to "Set-PodeState -Name \<name\> -Value \<value\>" would need a SetReplace value of "Set-PodeState -Name '{{name}}' -Value ".

```yaml
Type: String
Parameter Sets: Replace
Aliases:

Required: False
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
