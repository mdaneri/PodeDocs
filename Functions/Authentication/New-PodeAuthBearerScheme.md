---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# New-PodeAuthBearerScheme

## SYNOPSIS
Creates a new Bearer authentication scheme for Pode.

## SYNTAX

### Basic (Default)
```
New-PodeAuthBearerScheme [-BearerTag <String>] [-Location <String>] [-Scope <String[]>] [-AsJWT]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Bearer_HS
```
New-PodeAuthBearerScheme [-BearerTag <String>] [-Location <String>] [-Scope <String[]>] [-AsJWT]
 [-Algorithm <String[]>] -Secret <SecureString> [-JwtVerificationMode <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertFile
```
New-PodeAuthBearerScheme [-BearerTag <String>] [-Location <String>] [-Scope <String[]>] [-AsJWT]
 -Certificate <String> [-PrivateKeyPath <String>] [-CertificatePassword <SecureString>]
 [-RsaPaddingScheme <String>] [-JwtVerificationMode <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### CertThumb
```
New-PodeAuthBearerScheme [-BearerTag <String>] [-Location <String>] [-Scope <String[]>] [-AsJWT]
 -CertificateThumbprint <String> [-CertificateStoreName <StoreName>]
 [-CertificateStoreLocation <StoreLocation>] [-RsaPaddingScheme <String>] [-JwtVerificationMode <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertName
```
New-PodeAuthBearerScheme [-BearerTag <String>] [-Location <String>] [-Scope <String[]>] [-AsJWT]
 -CertificateName <String> [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>]
 [-RsaPaddingScheme <String>] [-JwtVerificationMode <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### CertRaw
```
New-PodeAuthBearerScheme [-BearerTag <String>] [-Location <String>] [-Scope <String[]>] [-AsJWT]
 -X509Certificate <X509Certificate> [-RsaPaddingScheme <String>] [-JwtVerificationMode <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertSelf
```
New-PodeAuthBearerScheme [-BearerTag <String>] [-Location <String>] [-Scope <String[]>] [-AsJWT] [-SelfSigned]
 [-RsaPaddingScheme <String>] [-JwtVerificationMode <String>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Defines a Bearer authentication scheme that allows authentication using a raw Bearer token or JWT.
Supports JWT validation with configurable security levels and token extraction from headers or query parameters.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAuthBearerScheme -AsJWT -Algorithm "HS256" -Secret (ConvertTo-SecureString "MySecretKey" -AsPlainText -Force)
```

### EXAMPLE 2
```
New-PodeAuthBearerScheme -AsJWT -Algorithm "RS256" -PrivateKey (Get-Content "private.pem" -Raw) -PublicKey (Get-Content "public.pem" -Raw)
```

## PARAMETERS

### -Algorithm
Accepted JWT signing algorithms:  HS256, HS384, HS512.

```yaml
Type: String[]
Parameter Sets: Bearer_HS
Aliases:

Required: False
Position: Named
Default value: @()
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJWT
Indicates if the Bearer token should be treated and validated as a JWT.

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

### -BearerTag
The header tag used for the Bearer token (default: "Bearer").

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

### -Certificate
The path to a certificate that can be use to enable HTTPS

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
A certificate subject name to use for RSA or ECDSA verification.
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
The password for the certificate file referenced in Certificate

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
The location of a certifcate store where a certificate can be found (Default: CurrentUser) (Windows).

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
The name of a certifcate store where a certificate can be found (Default: My) (Windows).

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
A certificate thumbprint to use for RSA or ECDSA verification.
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

### -JwtVerificationMode
JWT validation strictness: \`Strict\`, \`Moderate\`, or \`Lenient\` (default).

```yaml
Type: String
Parameter Sets: Bearer_HS, CertFile, CertThumb, CertName, CertRaw, CertSelf
Aliases:

Required: False
Position: Named
Default value: Lenient
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Specifies the token extraction location: \`Header\` (default) or \`Query\`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Header
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateKeyPath
A key file to be paired with a PEM certificate file referenced in Certificate

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
RSA padding scheme: \`Pkcs1V15\` (default) or \`Pss\`.

```yaml
Type: String
Parameter Sets: CertFile, CertThumb, CertName, CertRaw, CertSelf
Aliases:

Required: False
Position: Named
Default value: Pkcs1V15
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
A list of required scopes for the authentication scheme.

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

### -Secret
The HMAC secret key for JWT validation (required for HS256, HS384, HS512).

```yaml
Type: SecureString
Parameter Sets: Bearer_HS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelfSigned
Create and bind a self-signed CodeSigning ECSDA 384 Certificate.

```yaml
Type: SwitchParameter
Parameter Sets: CertSelf
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificate
The raw X509 certificate used for RSA or ECDSA verification.

```yaml
Type: X509Certificate
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

### [hashtable] - Returns the Bearer authentication scheme configuration.
## NOTES

## RELATED LINKS
