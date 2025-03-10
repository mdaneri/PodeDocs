---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Certificate
schema: 2.0.0
---

# New-PodeCertificateRequest

## SYNOPSIS
Generates a certificate signing request (CSR) and private key.

## SYNTAX

```
New-PodeCertificateRequest [[-DnsName] <String[]>] [[-CommonName] <String>] [[-Organization] <String>]
 [[-Locality] <String>] [[-State] <String>] [[-Country] <String>] [[-KeyType] <String>] [[-KeyLength] <Int32>]
 [[-CertificatePurpose] <String>] [[-EnhancedKeyUsages] <String[]>] [[-NotBefore] <DateTime>]
 [[-CustomExtensions] <Object[]>] [[-FriendlyName] <String>] [[-OutputPath] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function creates a certificate signing request (CSR) using RSA or ECDSA key pairs.
It allows specifying subject details, key usage, enhanced key usage (EKU), and custom extensions.
The CSR and private key are automatically saved to files in the specified output directory.

## EXAMPLES

### EXAMPLE 1
```
$csr = New-PodeCertificateRequest -DnsName "example.com" -CommonName "example.com" -KeyType "RSA" -KeyLength 2048
Generates an RSA CSR for "example.com" and saves it to the current working directory.
```

### EXAMPLE 2
```
$csr = New-PodeCertificateRequest -DnsName "example.com" -KeyType "ECDSA" -KeyLength 384 -CertificatePurpose "ServerAuth" -OutputPath "C:\Certs"
Generates an ECDSA CSR with an automatically assigned EKU for server authentication and saves it to "C:\Certs".
```

## PARAMETERS

### -CertificatePurpose
The intended purpose of the certificate, which automatically sets the EKU.
Supported values: 'ServerAuth', 'ClientAuth', 'CodeSigning', 'EmailSecurity', 'Custom'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommonName
The Common Name (CN) for the certificate subject.
Defaults to the first DNS name if not provided.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Country
The country (C) code (ISO 3166-1 alpha-2).
Defaults to 'XX'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: XX
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomExtensions
An array of additional custom certificate extensions.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsName
One or more DNS names (or IP addresses) to be included in the Subject Alternative Name (SAN).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnhancedKeyUsages
A list of OID strings for Enhanced Key Usage (EKU) if 'Custom' is selected as CertificatePurpose.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FriendlyName
An optional friendly name for the certificate request.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyLength
The key length for RSA (2048, 3072, 4096) or ECDSA (256, 384, 521).
Defaults to 2048.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
The cryptographic key type for the certificate request.
Supported values: 'RSA', 'ECDSA'.
Defaults to 'RSA'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### -Locality
The locality (L) name to be included in the certificate subject.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
The NotBefore date for the certificate request.
Defaults to the current UTC time.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: ([datetime]::UtcNow)
Accept pipeline input: False
Accept wildcard characters: False
```

### -Organization
The organization (O) name to be included in the certificate subject.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
The directory where the CSR and private key files will be saved.
Defaults to the current working directory.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: $PWD
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

### -State
The state (S) name to be included in the certificate subject.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### [PSCustomObject]
### Returns an object containing:
###   - CsrPath: The file path of the CSR.
###   - PrivateKeyPath: The file path of the private key.
## NOTES
- This function integrates with Pode's certificate handling utilities.
- The private key is exported in PKCS#8 format.
- Ensure the private key is stored securely.

## RELATED LINKS
