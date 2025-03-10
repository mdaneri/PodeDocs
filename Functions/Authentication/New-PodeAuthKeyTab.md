---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# New-PodeAuthKeyTab

## SYNOPSIS
A simple helper function, to help generate a new Keytab file for use with Kerberos authentication.

## SYNTAX

```
New-PodeAuthKeyTab [-Hostname] <String> [-DomainName] <String> [-Username] <String> [[-Password] <String>]
 [[-FilePath] <String>] [[-Crypto] <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
A simple helper function, to help generate a new Keytab file for use with Kerberos authentication.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAuthKeyTab -Hostname 'pode.example.com' -DomainName 'example.com' -Username 'example\pode_user'
```

### EXAMPLE 2
```
New-PodeAuthKeyTab -Hostname 'pode.example.com' -DomainName 'example.com' -Username 'example\pode_user' -Password 'pa$$word!'
```

### EXAMPLE 3
```
New-PodeAuthKeyTab -Hostname 'pode.example.com' -DomainName 'example.com' -Username 'example\pode_user' -FilePath 'custom_name.keytab'
```

### EXAMPLE 4
```
New-PodeAuthKeyTab -Hostname 'pode.example.com' -DomainName 'example.com' -Username 'example\pode_user' -Crypto 'AES256-SHA1'
```

## PARAMETERS

### -Crypto
The Encryption type to use for the Keytab file.
(Default: All)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: All
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName
The Domain Name to use for the Keytab file.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
The File Path to save the Keytab file.
(Default: pode.keytab)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: Pode.keytab
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hostname
The Hostname to use for the Keytab file.

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

### -Password
The Password to use for the Keytab file.
(Default: * - this will prompt for a password)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: *
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

### -Username
The Username to use for the Keytab file.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
This function uses the ktpass command to generate the Keytab file.

## RELATED LINKS
