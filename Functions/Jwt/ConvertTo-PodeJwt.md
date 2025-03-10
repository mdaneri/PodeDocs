---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Jwt
schema: 2.0.0
---

# ConvertTo-PodeJwt

## SYNOPSIS
Generates a JSON Web Token (JWT) based on the specified headers, payload, and signing credentials.

## SYNTAX

### Default (Default)
```
ConvertTo-PodeJwt [-Header <Hashtable>] -Payload <Hashtable> [-Algorithm <String>] [-Expiration <Int32>]
 [-NotBefore <Int32>] [-IssuedAt <Int32>] [-Issuer <String>] [-Subject <String>] [-Audience <String>]
 [-JwtId <String>] [-NoStandardClaims] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Secret
```
ConvertTo-PodeJwt [-Header <Hashtable>] -Payload <Hashtable> [-Algorithm <String>] -Secret <Object>
 [-Expiration <Int32>] [-NotBefore <Int32>] [-IssuedAt <Int32>] [-Issuer <String>] [-Subject <String>]
 [-Audience <String>] [-JwtId <String>] [-NoStandardClaims] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### CertRaw
```
ConvertTo-PodeJwt [-Header <Hashtable>] -Payload <Hashtable> -X509Certificate <X509Certificate2>
 [-RsaPaddingScheme <String>] [-Expiration <Int32>] [-NotBefore <Int32>] [-IssuedAt <Int32>] [-Issuer <String>]
 [-Subject <String>] [-Audience <String>] [-JwtId <String>] [-NoStandardClaims]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertFile
```
ConvertTo-PodeJwt [-Header <Hashtable>] -Payload <Hashtable> -Certificate <String> [-PrivateKeyPath <String>]
 [-CertificatePassword <SecureString>] [-RsaPaddingScheme <String>] [-Expiration <Int32>] [-NotBefore <Int32>]
 [-IssuedAt <Int32>] [-Issuer <String>] [-Subject <String>] [-Audience <String>] [-JwtId <String>]
 [-NoStandardClaims] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertThumb
```
ConvertTo-PodeJwt [-Header <Hashtable>] -Payload <Hashtable> -CertificateThumbprint <String>
 [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>] [-RsaPaddingScheme <String>]
 [-Expiration <Int32>] [-NotBefore <Int32>] [-IssuedAt <Int32>] [-Issuer <String>] [-Subject <String>]
 [-Audience <String>] [-JwtId <String>] [-NoStandardClaims] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### CertName
```
ConvertTo-PodeJwt [-Header <Hashtable>] -Payload <Hashtable> -CertificateName <String>
 [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>] [-RsaPaddingScheme <String>]
 [-Expiration <Int32>] [-NotBefore <Int32>] [-IssuedAt <Int32>] [-Issuer <String>] [-Subject <String>]
 [-Audience <String>] [-JwtId <String>] [-NoStandardClaims] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### AuthenticationMethod
```
ConvertTo-PodeJwt [-Header <Hashtable>] -Payload <Hashtable> -Authentication <String> [-Expiration <Int32>]
 [-NotBefore <Int32>] [-IssuedAt <Int32>] [-Issuer <String>] [-Subject <String>] [-Audience <String>]
 [-JwtId <String>] [-NoStandardClaims] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function creates a JWT by combining a Base64URL-encoded header and payload.
Depending on the
configured parameters, it supports various signing algorithms, including HMAC- and certificate-based
signatures.
You can also omit a signature by specifying 'none'.

## EXAMPLES

### EXAMPLE 1
```
ConvertTo-PodeJwt -Header @{ alg = 'none' } -Payload @{ sub = '123'; name = 'John' }
```

### EXAMPLE 2
```
ConvertTo-PodeJwt -Header @{ alg = 'HS256' } -Payload @{ sub = '123'; name = 'John' } -Secret 'abc'
```

### EXAMPLE 3
```
ConvertTo-PodeJwt -Header @{ alg = 'RS256' } -Payload @{ sub = '123' } -PrivateKey (Get-Content "private.pem" -Raw) -Issuer "auth.example.com" -Audience "myapi.example.com"
```

## PARAMETERS

### -Algorithm
A string representing the signing algorithm to be used.
Accepts 'NONE', 'HS256', 'HS384', or 'HS512'.

```yaml
Type: String
Parameter Sets: Default, Secret
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Audience
Specifies the recipients that the token is intended for.

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

### -Authentication
The name of a configured authentication method in Pode.
Required if you select the 'AuthenticationMethod' parameter set.

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
Required if you select the 'CertFile' parameter set.

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
A string name of a certificate in the local store.
Required if you select the 'CertName' parameter set.

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
An optional SecureString password for a certificate file.

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
The certificate store location for the specified certificate.
Defaults to 'CurrentUser'.

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
The store name to search for the specified certificate.
Defaults to 'My'.

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
A string thumbprint of a certificate in the local store.
Required if you select the 'CertThumb' parameter set.

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

### -Expiration
Time in seconds until the token expires.
Defaults to 3600 (1 hour).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3600
Accept pipeline input: False
Accept wildcard characters: False
```

### -Header
Additional header values for the JWT.
Defaults to an empty hashtable if not specified.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: @{}
Accept pipeline input: False
Accept wildcard characters: False
```

### -IssuedAt
Time in seconds to offset the IssuedAt claim.
Defaults to 0 for current time.

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

### -Issuer
Identifies the principal that issued the token.

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

### -JwtId
A unique identifier for the token.

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

### -NoStandardClaims
A switch that, if used, prevents automatically adding iat, nbf, exp, iss, sub, aud, and jti claims.

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

### -NotBefore
Time in seconds to offset the NotBefore claim.
Defaults to 0 for immediate use.

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

### -Payload
The required hashtable specifying the token's claims.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateKeyPath
Optional path to an associated certificate key file.

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
Specifies the RSA padding scheme to use.
Accepts 'Pkcs1V15' or 'Pss'.
Defaults to 'Pkcs1V15'.

```yaml
Type: String
Parameter Sets: CertRaw, CertFile, CertThumb, CertName
Aliases:

Required: False
Position: Named
Default value: Pkcs1V15
Accept pipeline input: False
Accept wildcard characters: False
```

### -Secret
Used in conjunction with HMAC signing.
Can be either a byte array or a SecureString.
Required if you
select the 'Secret' parameter set.

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

### -Subject
Identifies the principal that is the subject of the token.

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

### -X509Certificate
An X509Certificate2 object used for RSA/ECDSA-based signing.
Required if you select the 'CertRaw' parameter set.

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

### System.String
### The resulting JWT string.
## NOTES

## RELATED LINKS
