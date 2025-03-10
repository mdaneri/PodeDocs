---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# New-PodeAuthDigestScheme

## SYNOPSIS
Creates a new Digest authentication scheme for Pode.

## SYNTAX

### Basic (Default)
```
New-PodeAuthDigestScheme [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Digest
```
New-PodeAuthDigestScheme [-HeaderTag <String>] [-Algorithm <String[]>] [-QualityOfProtection <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function defines a Digest authentication scheme in Pode.
It allows specifying
parameters such as the authentication algorithm, quality of protection, and an optional
header tag.
The function ensures secure authentication by leveraging Pode's built-in
digest authentication mechanisms.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAuthDigestScheme -Algorithm 'SHA-256' -QualityOfProtection 'auth-int'
```

This example creates a new Digest authentication scheme using SHA-256 and sets
the Quality of Protection to 'auth-int'.

## PARAMETERS

### -Algorithm
Specifies the digest algorithm used for authentication.
The default is 'MD5'.
Other supported values include 'SHA-1', 'SHA-256', 'SHA-512', 'SHA-384', and 'SHA-512/256'.

```yaml
Type: String[]
Parameter Sets: Digest
Aliases:

Required: False
Position: Named
Default value: MD5
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeaderTag
An optional custom header tag for the authentication scheme.
Defaults to 'Digest'.

```yaml
Type: String
Parameter Sets: Digest
Aliases:

Required: False
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

### -QualityOfProtection
Determines the Quality of Protection (QoP) setting for authentication.
The default is 'auth'.
Available options are 'auth', 'auth-int', and 'auth,auth-int'.

```yaml
Type: String[]
Parameter Sets: Digest
Aliases:

Required: False
Position: Named
Default value: Auth
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Hashtable containing the defined Digest authentication scheme for Pode.
## NOTES
Internal function for Pode authentication schemes.
Subject to change in future updates.

## RELATED LINKS
