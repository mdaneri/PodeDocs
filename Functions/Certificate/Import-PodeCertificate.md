---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Certificate
schema: 2.0.0
---

# Import-PodeCertificate

## SYNOPSIS
Imports an X.509 certificate from a file (PFX, PEM, CER) or retrieves it from the Windows certificate store.

## SYNTAX

### CertFile
```
Import-PodeCertificate -Path <String> [-PrivateKeyPath <String>] [-CertificatePassword <SecureString>]
 [-Exportable] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertThumb
```
Import-PodeCertificate [-Exportable] -CertificateThumbprint <String> [-CertificateStoreName <StoreName>]
 [-CertificateStoreLocation <StoreLocation>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertName
```
Import-PodeCertificate [-Exportable] -CertificateName <String> [-CertificateStoreName <StoreName>]
 [-CertificateStoreLocation <StoreLocation>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function imports an X.509 certificate using one of three methods:
  - From a certificate file (PFX, PEM, or CER).
  - From the Windows certificate store by thumbprint.
  - From the Windows certificate store by subject name.

By default, the certificate is imported with an **ephemeral key**, meaning the private key
exists **only for the current session** and is not persisted.
If the \`-Persistent\` flag is
specified, the private key will be stored in an exportable format.

## EXAMPLES

### EXAMPLE 1
```
$cert = Import-PodeCertificate -Path "C:\Certs\mycert.pfx" -CertificatePassword (ConvertTo-SecureString -String "MyPass" -AsPlainText -Force)
Imports a PFX certificate file with an ephemeral private key.
```

### EXAMPLE 2
```
$cert = Import-PodeCertificate -Path "C:\Certs\mycert.pfx" -CertificatePassword (ConvertTo-SecureString -String "MyPass" -AsPlainText -Force) -Persistent
Imports a PFX certificate file **with a persistent private key**, allowing it to be saved.
```

### EXAMPLE 3
```
$cert = Import-PodeCertificate -Path "C:\Certs\mycert.cer"
Imports a CER certificate file (public key only).
```

### EXAMPLE 4
```
$cert = Import-PodeCertificate -CertificateThumbprint "D2C2F4F7A456B69D4F9E9F8C3D3D6E5A9C3EBA6F"
Retrieves a certificate from the Windows certificate store using its thumbprint.
```

### EXAMPLE 5
```
$cert = Import-PodeCertificate -CertificateName "MyAppCert" -CertificateStoreName "Root" -CertificateStoreLocation "LocalMachine"
Retrieves a certificate by subject name from the LocalMachine\Root store.
```

## PARAMETERS

### -CertificateName
The subject name of a certificate stored in the Windows certificate store.

```yaml
Type: String
Parameter Sets: CertName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
A secure string containing the password for decrypting a PFX certificate
or an encrypted private key in PEM format.

```yaml
Type: SecureString
Parameter Sets: CertFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateStoreLocation
The location of the Windows certificate store.
Defaults to "CurrentUser".

```yaml
Type: StoreLocation
Parameter Sets: CertThumb, CertName
Aliases:
Accepted values: CurrentUser, LocalMachine

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateStoreName
The name of the Windows certificate store to search in when retrieving a certificate
by thumbprint or subject name.
Defaults to "My".

```yaml
Type: StoreName
Parameter Sets: CertThumb, CertName
Aliases:
Accepted values: AddressBook, AuthRoot, CertificateAuthority, Disallowed, My, Root, TrustedPeople, TrustedPublisher

Required: False
Position: Named
Default value: My
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
The thumbprint of a certificate stored in the Windows certificate store.

```yaml
Type: String
Parameter Sets: CertThumb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exportable
If specified, the certificate will be imported with an **exportable** private key,
allowing it to be saved and reused across sessions.

If not specified, the certificate will be imported **ephemerally**, meaning the
private key will exist **only in memory** and will be lost when the process exits.

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

### -Path
The path to the certificate file (.pfx, .pem, or .cer) to import.

```yaml
Type: String
Parameter Sets: CertFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateKeyPath
The path to a separate private key file (for PEM format).
Required if the certificate file does not contain the private key.

```yaml
Type: String
Parameter Sets: CertFile
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

### [System.Security.Cryptography.X509Certificates.X509Certificate2]
### Returns the imported certificate as an X509Certificate2 object.
## NOTES
- The \`-Persistent\` flag should be used when you need to store the certificate for future use.
- The default behavior (\`EphemeralKeySet\`) ensures the private key does not persist in the system.
- When using a PEM certificate, ensure the private key is available if required.
- Windows certificate store retrieval is only supported on Windows systems.
- CER files contain only the public key and do not support private key decryption.
- The improrted Certificate is not validated and returned as is.

## RELATED LINKS
