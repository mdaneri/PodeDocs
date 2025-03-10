---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Jwt
schema: 2.0.0
---

# Update-PodeJwt

## SYNOPSIS
Updates the expiration time of a JWT token.

## SYNTAX

### Default (Default)
```
Update-PodeJwt [-ExpirationExtension <Int32>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertFile
```
Update-PodeJwt -Token <String> [-ExpirationExtension <Int32>] -Certificate <String> [-PrivateKeyPath <String>]
 [-CertificatePassword <SecureString>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertRaw
```
Update-PodeJwt -Token <String> [-ExpirationExtension <Int32>] -X509Certificate <X509Certificate2>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertThumb
```
Update-PodeJwt -Token <String> [-ExpirationExtension <Int32>] -CertificateThumbprint <String>
 [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertName
```
Update-PodeJwt -Token <String> [-ExpirationExtension <Int32>] -CertificateName <String>
 [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Secret
```
Update-PodeJwt -Token <String> [-ExpirationExtension <Int32>] -Secret <Object>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### AuthenticationMethod
```
Update-PodeJwt [-ExpirationExtension <Int32>] -Authentication <String> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This function updates the expiration time of a given JWT token by extending it with a specified duration.
It supports various signing methods including secret-based and certificate-based signing.
The function can handle different types of certificates and authentication methods for signing the updated token.

## EXAMPLES

### EXAMPLE 1
```
" -ExpirationExtension 3600 -Secret "MySecretKey"
This example updates the expiration time of a JWT token by extending it by 1 hour using an HMAC secret.
```

### EXAMPLE 2
```
" -ExpirationExtension 3600 -X509Certificate $Certificate
This example updates the expiration time of a JWT token by extending it by 1 hour using an X509 certificate.
```

## PARAMETERS

### -Authentication
The authentication method from Pode's context used for JWT signing.

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
The path to a certificate file used for signing.

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
A certificate subject name to use for RSA or ECDSA signing.
(Windows).

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
The password for the certificate file referenced in Certificate.

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
The location of a certificate store where a certificate can be found (Default: CurrentUser) (Windows).

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
The name of a certificate store where a certificate can be found (Default: My) (Windows).

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
A certificate thumbprint to use for RSA or ECDSA signing.
(Windows).

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

### -ExpirationExtension
The number of seconds to extend the expiration time by.
If not specified, the original expiration duration is used.

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

### -PrivateKeyPath
A key file to be paired with a PEM certificate file referenced in Certificate.

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

### -Secret
The secret key used for HMAC signing (string or byte array).

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
The JWT token to be updated.

```yaml
Type: String
Parameter Sets: CertFile, CertRaw, CertThumb, CertName, Secret
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificate
The raw X509 certificate used for RSA or ECDSA signing.

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

## NOTES

## RELATED LINKS
