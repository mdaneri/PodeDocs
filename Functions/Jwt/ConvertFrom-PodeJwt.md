---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Jwt
schema: 2.0.0
---

# ConvertFrom-PodeJwt

## SYNOPSIS
Converts a JWT token into a PowerShell object, optionally verifying its signature.

## SYNTAX

### Default (Default)
```
ConvertFrom-PodeJwt [-IgnoreSignature] [-Outputs <String>] [-HumanReadable]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### AuthenticationMethod
```
ConvertFrom-PodeJwt [-Token <String>] [-Outputs <String>] [-HumanReadable] -Authentication <String>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Ignore
```
ConvertFrom-PodeJwt -Token <String> [-IgnoreSignature] [-Outputs <String>] [-HumanReadable]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertFile
```
ConvertFrom-PodeJwt -Token <String> [-Outputs <String>] [-HumanReadable] -Certificate <String>
 [-PrivateKeyPath <String>] [-CertificatePassword <SecureString>] [-RsaPaddingScheme <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertRaw
```
ConvertFrom-PodeJwt -Token <String> [-Outputs <String>] [-HumanReadable] -X509Certificate <X509Certificate2>
 [-RsaPaddingScheme <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertThumb
```
ConvertFrom-PodeJwt -Token <String> [-Outputs <String>] [-HumanReadable] -CertificateThumbprint <String>
 [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>] [-RsaPaddingScheme <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertName
```
ConvertFrom-PodeJwt -Token <String> [-Outputs <String>] [-HumanReadable] -CertificateName <String>
 [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>] [-RsaPaddingScheme <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Secret
```
ConvertFrom-PodeJwt -Token <String> [-Outputs <String>] [-HumanReadable] -Secret <Object>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The ConvertFrom-PodeJwt function takes a JWT token and decodes its header, payload,
and signature.
By default, it verifies the signature using a specified secret,
certificate, or Pode authentication method.
If IgnoreSignature is specified,
the function decodes and returns the token payload without verification.

## EXAMPLES

### EXAMPLE 1
```
ConvertFrom-PodeJwt -Token $jwtToken -Secret 'mysecret'
Decodes and verifies the JWT token using an HMAC secret.
```

### EXAMPLE 2
```
ConvertFrom-PodeJwt -Token $jwtToken -Certificate './certs/myCert.pem'
Decodes and verifies the JWT token using an X.509 certificate from a file.
```

## PARAMETERS

### -Authentication
A Pode authentication method name whose configuration is used
for signature verification.

```yaml
Type: String
Parameter Sets: AuthenticationMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificate
The path to a file containing an X.509 certificate for RSA/ECDSA signature verification.

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

### -CertificateName
A subject name to retrieve a certificate from the Windows certificate store.

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
A SecureString containing a password for the certificate file, if required.

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
The location of the Windows certificate store to search (default: CurrentUser).

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
The name of the Windows certificate store to search (default: My).

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
A thumbprint to retrieve a certificate from the Windows certificate store.

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

### -HumanReadable
Converts UNIX timestamps (e.g., iat, nbf, exp) into DateTime objects for easier reading.

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

### -IgnoreSignature
Indicates that the JWT token signature should be ignored
and the payload returned directly without verification.

```yaml
Type: SwitchParameter
Parameter Sets: Default, Ignore
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Outputs
Determines which parts of the JWT should be returned:
Header, Payload, Signature, or any combination thereof.
Defaults to 'Payload'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Payload
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateKeyPath
The path to a PEM key file that pairs with the certificate
for RSA/ECDSA signature verification.

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

### -RsaPaddingScheme
Specifies the RSA padding scheme to use (Pkcs1V15 or Pss).
Defaults to Pkcs1V15.

```yaml
Type: String
Parameter Sets: CertFile, CertRaw, CertThumb, CertName
Aliases:

Required: False
Position: Named
Default value: Pkcs1V15
Accept pipeline input: False
Accept wildcard characters: False
```

### -Secret
A string or byte array used for HMAC-based signature verification.

```yaml
Type: Object
Parameter Sets: Secret
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Token
The JWT token to be decoded and optionally verified.

```yaml
Type: String
Parameter Sets: AuthenticationMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Ignore, CertFile, CertRaw, CertThumb, CertName, Secret
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificate
A raw X.509 certificate object used for RSA/ECDSA signature verification.

```yaml
Type: X509Certificate2
Parameter Sets: CertRaw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### [pscustomobject] or [System.Collections.Specialized.OrderedDictionary].
### Returns one or more parts of the JWT (Header, Payload, Signature)
### as PowerShell objects or dictionaries.
## NOTES
- This function is tailored for use with Pode, a PowerShell web server framework.
- When signature verification is enabled, the appropriate key or certificate must be provided.
- Use HTTPS in production to safeguard tokens.

## RELATED LINKS
