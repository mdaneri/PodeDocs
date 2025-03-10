---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Get-PodeAuthUser

## SYNOPSIS
Get the authenticated user from the WebEvent or Session.

## SYNTAX

```
Get-PodeAuthUser [-IgnoreSession] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Get the authenticated user from the WebEvent or Session.
This is similar to calling $Webevent.Auth.User.

## EXAMPLES

### EXAMPLE 1
```
$user = Get-PodeAuthUser
```

## PARAMETERS

### -IgnoreSession
If supplied, only the Auth object in the WebEvent will be used and the Session will be skipped.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
