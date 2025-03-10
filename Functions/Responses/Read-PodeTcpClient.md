---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Responses
schema: 2.0.0
---

# Read-PodeTcpClient

## SYNOPSIS
Reads data from a TCP socket stream.

## SYNTAX

### default (Default)
```
Read-PodeTcpClient [-Timeout <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CheckBytes
```
Read-PodeTcpClient [-Timeout <Int32>] [-CheckBytes <Byte[]>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### CRLF
```
Read-PodeTcpClient [-Timeout <Int32>] [-CRLFMessageEnd] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Reads data from a TCP socket stream.

## EXAMPLES

### EXAMPLE 1
```
$data = Read-PodeTcpClient
```

### EXAMPLE 2
```
$data = Read-PodeTcpClient -CRLFMessageEnd
```

## PARAMETERS

### -CheckBytes
An optional array of bytes to check at the end of a receievd data stream, to determine if the data is complete.

```yaml
Type: Byte[]
Parameter Sets: CheckBytes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CRLFMessageEnd
If supplied, the CheckBytes will be set to 13 and 10 to make sure a message ends with CR and LF.

```yaml
Type: SwitchParameter
Parameter Sets: CRLF
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

### -Timeout
An optional Timeout in milliseconds.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.String
## NOTES

## RELATED LINKS
