---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Service
schema: 2.0.0
---

# Unregister-PodeService

## SYNOPSIS
Unregisters a Pode-based service across different platforms (Windows, Linux, and macOS).

## SYNTAX

```
Unregister-PodeService [-Name] <String> [-Force] [-Agent] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
The \`Unregister-PodeService\` function removes a Pode-based service by checking its status and unregistering it from the system.
The function can stop the service forcefully if it is running, and then remove the service from the service manager.
It works on Windows, Linux (systemd), and macOS (launchctl).

## EXAMPLES

### EXAMPLE 1
```
Unregister-PodeService -Force
```

Unregisters the Pode-based service, forcefully stopping it if it is currently running.

### EXAMPLE 2
```
Unregister-PodeService
```

Unregisters the Pode-based service if it is not running.
If the service is running, the function throws an error unless the \`-Force\` parameter is used.

## PARAMETERS

### -Agent
Specifies that only agent-type services should be returned.
This parameter is applicable to macOS only.

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

### -Force
A switch parameter that forces the service to stop before unregistering.
If the service is running and this parameter is not specified,
the function will throw an error.

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

### -Name
The name of the service.

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
- The function retrieves the service name from the \`srvsettings.json\` file located in the script directory.
- On Windows, it uses \`Get-Service\`, \`Stop-Service\`, and \`Remove-Service\`.
- On Linux, it uses \`systemctl\` to stop, disable, and remove the service.
- On macOS, it uses \`launchctl\` to stop and unload the service.

## RELATED LINKS
