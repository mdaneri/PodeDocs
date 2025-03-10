---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Sessions
schema: 2.0.0
---

# Get-PodeSessionId

## SYNOPSIS
Returns the currently authenticated SessionId.

## SYNTAX

```
Get-PodeSessionId [-Signed] [-Force] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns the currently authenticated SessionId.
If there's no session, or it's not authenticated, then null is returned instead.
You can also have the SessionId returned as signed as well.

## EXAMPLES

### EXAMPLE 1
```
$sessionId = Get-PodeSessionId
```

## PARAMETERS

### -Force
If supplied, the sessionId will be returned regardless of authentication.

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

### -Signed
If supplied, the returned SessionId will also be signed.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
