---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Service
schema: 2.0.0
---

# Get-PodeService

## SYNOPSIS
Retrieves the status of a Pode service across different platforms (Windows, Linux, and macOS).

## SYNTAX

```
Get-PodeService [-Name] <String> [-Agent] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The \`Get-PodeService\` function checks if a Pode-based service is running or stopped on the host system.
It supports Windows (using \`Get-Service\`), Linux (using \`systemctl\`), and macOS (using \`launchctl\`).
The function returns a consistent result across all platforms by providing the service name and status in
a hashtable format.
The status is mapped to common states like "Running," "Stopped," "Starting," and "Stopping."

## EXAMPLES

### EXAMPLE 1
```
Get-PodeService
```

Retrieves the current status of the Pode service defined in the \`srvsettings.json\` configuration file.

### EXAMPLE 2
```
Get-PodeService
```

On Windows:
@{ Name = "MyService"; Status = "Running" }

On Linux:
@{ Name = "MyService"; Status = "Stopped" }

On macOS:
@{ Name = "MyService"; Status = "Unknown" }

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

### Hashtable
###     The function returns a hashtable containing the service name and its status.
###     For example: @{ Name = "MyService"; Status = "Running" }
## NOTES
- The function reads the service name from the \`srvsettings.json\` file in the script's directory.
- For Windows, it uses the \`Get-Service\` cmdlet.
- For Linux, it uses \`systemctl\` to retrieve the service status.
- For macOS, it uses \`launchctl\` to check if the service is running.

## RELATED LINKS
