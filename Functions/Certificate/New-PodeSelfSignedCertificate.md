---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Certificate
schema: 2.0.0
---

# New-PodeSelfSignedCertificate

## SYNOPSIS
Generates a self-signed X.509 certificate.

## SYNTAX

### CommonName (Default)
```
New-PodeSelfSignedCertificate [-CommonName <String>] [-Password <SecureString>] [-Organization <String>]
 [-Locality <String>] [-State <String>] [-Country <String>] [-KeyType <String>] [-KeyLength <Int32>]
 [-EnhancedKeyUsages <String[]>] [-CertificatePurpose <String>] [-NotBefore <DateTime>]
 [-CustomExtensions <Object[]>] [-FriendlyName <String>] [-ValidityDays <Int32>] [-Ephemeral] [-Exportable]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### DnsName
```
New-PodeSelfSignedCertificate [-DnsName <String[]>] [-Loopback] [-Password <SecureString>]
 [-Organization <String>] [-Locality <String>] [-State <String>] [-Country <String>] [-KeyType <String>]
 [-KeyLength <Int32>] [-EnhancedKeyUsages <String[]>] [-CertificatePurpose <String>] [-NotBefore <DateTime>]
 [-CustomExtensions <Object[]>] [-FriendlyName <String>] [-ValidityDays <Int32>] [-Ephemeral] [-Exportable]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function creates a self-signed X.509 certificate using RSA or ECDSA key pairs.
It supports specifying subject details, key usage, enhanced key usage (EKU),
and custom extensions.
The generated certificate is returned as an X509Certificate2 object.

By default, the private key is exportable so the certificate can be saved and reused.
If the \`-Ephemeral\` parameter is specified, the certificate's private key **will not be persisted**
and will only exist in memory for the current session.

## EXAMPLES

### EXAMPLE 1
```
$cert = New-PodeSelfSignedCertificate -Loopback
Creates a self-signed certificate for local addresses (`127.0.0.1`, `::1`, `localhost`, machine hostname).
```

### EXAMPLE 2
```
$cert = New-PodeSelfSignedCertificate -DnsName "example.com" -KeyType "RSA" -KeyLength 2048
Creates a self-signed RSA certificate for "example.com" with a 2048-bit key, valid for 365 days.
```

### EXAMPLE 3
```
$cert = New-PodeSelfSignedCertificate -DnsName "internal.local" -Ephemeral
Creates a self-signed certificate with a private key that exists **only in memory** for the current session.
```

### EXAMPLE 4
```
$cert = New-PodeSelfSignedCertificate -DnsName "testserver.local" -KeyType "ECDSA" -KeyLength 384 -CertificatePurpose "ClientAuth" -ValidityDays 730
Generates a self-signed ECDSA certificate for "testserver.local" with client authentication EKU, valid for 730 days.
```

## PARAMETERS

### -CertificatePurpose
The intended purpose of the certificate, which automatically sets the EKU.
Supported values: 'ServerAuth', 'ClientAuth', 'CodeSigning', 'EmailSecurity', 'Custom'.
Defaults to 'ServerAuth'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: ServerAuth
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommonName
The Common Name (CN) for the certificate subject.
Defaults to "SelfSigned".

```yaml
Type: String
Parameter Sets: CommonName
Aliases:

Required: False
Position: Named
Default value: SelfSigned
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
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsName
One or more DNS names (or IP addresses) to be included in the Subject Alternative Name (SAN).

```yaml
Type: String[]
Parameter Sets: DnsName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnhancedKeyUsages
A list of OID strings for Enhanced Key Usage (EKU), e.g., '1.3.6.1.5.5.7.3.1' for server authentication.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ephemeral
If specified, the certificate will be created with \`EphemeralKeySet\`, meaning the private key
will **not be persisted** on disk or in the certificate store.

This is useful for temporary certificates that should only exist in memory for the duration
of the current session.
Once the process exits, the private key will be lost.

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

### -Exportable
If specified the certificate will be created with \`Exportable\`, meaning the certificate can be exported

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

### -FriendlyName
A friendly name for the certificate, used when storing it in a certificate store.
Defaults to 'MyCertificate'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: MyCertificate
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
Position: Named
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
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Loopback
If specified, automatically sets \`DnsName\` to include:
  - \`127.0.0.1\`, \`::1\`, \`localhost\`
  - The current machine's IP (if not local)
  - The Pode server's hostname and FQDN (if available)

```yaml
Type: SwitchParameter
Parameter Sets: DnsName
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
The NotBefore date for the certificate validity start.
Defaults to the current UTC time.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Specifies an optional password for protecting the exported PFX.
If not provided, the PFX will be unprotected.

```yaml
Type: SecureString
Parameter Sets: (All)
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

### -State
The state (S) name to be included in the certificate subject.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidityDays
The number of days the certificate will remain valid.
Defaults to 365 days.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 365
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### [System.Security.Cryptography.X509Certificates.X509Certificate2]
### Returns the generated self-signed certificate as an X509Certificate2 object.
## NOTES
- The private key is embedded in the generated certificate.
- By default, the certificate is **exportable** so it can be saved and reused.
- If \`-Ephemeral\` is used, the private key will **only exist in memory** and cannot be exported or stored.
- The \`-Loopback\` parameter is useful for local development, ensuring the certificate includes local identifiers.

## RELATED LINKS
