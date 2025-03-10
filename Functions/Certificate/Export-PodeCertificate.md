---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Certificate
schema: 2.0.0
---

# Export-PodeCertificate

## SYNOPSIS
Exports an X.509 certificate to a file (PFX, PEM, or CER) or installs it into the Windows certificate store.

## SYNTAX

### File (Default)
```
Export-PodeCertificate -Certificate <X509Certificate2> [-Path <String>] [-Format <String>]
 [-CertificatePassword <SecureString>] [-IncludePrivateKey] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### WindowsStore
```
Export-PodeCertificate -Certificate <X509Certificate2> -CertificateStoreName <StoreName>
 -CertificateStoreLocation <StoreLocation> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function exports an X.509 certificate in various formats:
  - PFX (PKCS#12) with optional password protection.
  - PEM (Base64-encoded format), optionally including the private key.
  - CER (DER-encoded format).
It also allows storing the certificate in the Windows certificate store.

The function supports exporting private keys (if available) for PEM format, encrypting them if a password is provided.

## EXAMPLES

### EXAMPLE 1
```
$cert = Get-PodeCertificate -Path "mycert.pfx" -Password (ConvertTo-SecureString -String "MyPass" -AsPlainText -Force)
Export-PodeCertificate -Certificate $cert -Path "C:\Certs\mycert" -Format "PEM" -IncludePrivateKey
```

Exports the certificate as a PEM file with a separate private key file.

### EXAMPLE 2
```
$cert = Get-PodeCertificate -Path "mycert.pfx" -Password (ConvertTo-SecureString -String "MyPass" -AsPlainText -Force)
Export-PodeCertificate -Certificate $cert -CertificateStoreName "My" -CertificateStoreLocation "LocalMachine"
```

Stores the certificate in the LocalMachine certificate store under "My".

## PARAMETERS

### -Certificate
The X509Certificate2 object to export.
This must be a valid certificate.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertificatePassword
A secure string containing the password for exporting the PFX format
or encrypting the private key in PEM format.

```yaml
Type: SecureString
Parameter Sets: File
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateStoreLocation
The location of the Windows certificate store.
Defaults to 'CurrentUser'.
This parameter is required when using the 'WindowsStore' parameter set.

```yaml
Type: StoreLocation
Parameter Sets: WindowsStore
Aliases:
Accepted values: CurrentUser, LocalMachine

Required: True
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateStoreName
The Windows certificate store name where the certificate should be installed.
This parameter is required when using the 'WindowsStore' parameter set.

```yaml
Type: StoreName
Parameter Sets: WindowsStore
Aliases:
Accepted values: AddressBook, AuthRoot, CertificateAuthority, Disallowed, My, Root, TrustedPeople, TrustedPublisher

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Format
The format in which to export the certificate.
Supported values: 'PFX', 'PEM', 'CER'.
Defaults to 'PFX'.

```yaml
Type: String
Parameter Sets: File
Aliases:

Required: False
Position: Named
Default value: PFX
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludePrivateKey
When exporting in PEM format, this flag includes the private key in a separate \`.key\` file.

```yaml
Type: SwitchParameter
Parameter Sets: File
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The output file path (without an extension) where the certificate will be saved.
Defaults to the current working directory with the certificate subject name.

```yaml
Type: String
Parameter Sets: File
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### [string] or [hashtable]
### - If exporting to a file, returns the full file path(s) of the exported certificate.
### - If storing in Windows, returns `$true` if successful, `$false` otherwise.
## NOTES
- This function integrates with Pode's certificate handling utilities.
- Windows store installation is only available on Windows.
- PEM format supports exporting the private key separately, which can be encrypted with a password.

## RELATED LINKS
