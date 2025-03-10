---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Endpoint
schema: 2.0.0
---

# Add-PodeEndpoint

## SYNOPSIS
Bind an endpoint to listen for incoming Requests.

## SYNTAX

### Default (Default)
```
Add-PodeEndpoint [-Address <String>] [-Port <Int32>] [-Hostname <String>] [-Protocol <String>] [-Name <String>]
 [-RedirectTo <String>] [-Description <String>] [-Acknowledge <String>] [-SslProtocol <String[]>]
 [-CRLFMessageEnd] [-Force] [-AllowClientCertificate] [-PassThru] [-LookupHostname] [-DualMode] [-Default]
 [-Favicon <Byte[]>] [-DefaultFavicon] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertFile
```
Add-PodeEndpoint [-Address <String>] [-Port <Int32>] [-Hostname <String>] [-Protocol <String>]
 -Certificate <String> [-CertificatePassword <Object>] [-CertificateKey <String>] [-TlsMode <String>]
 [-Name <String>] [-RedirectTo <String>] [-Description <String>] [-Acknowledge <String>]
 [-SslProtocol <String[]>] [-CRLFMessageEnd] [-Force] [-AllowClientCertificate] [-PassThru] [-LookupHostname]
 [-DualMode] [-Default] [-Favicon <Byte[]>] [-DefaultFavicon] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### CertThumb
```
Add-PodeEndpoint [-Address <String>] [-Port <Int32>] [-Hostname <String>] [-Protocol <String>]
 -CertificateThumbprint <String> [-CertificateStoreName <StoreName>]
 [-CertificateStoreLocation <StoreLocation>] [-TlsMode <String>] [-Name <String>] [-RedirectTo <String>]
 [-Description <String>] [-Acknowledge <String>] [-SslProtocol <String[]>] [-CRLFMessageEnd] [-Force]
 [-AllowClientCertificate] [-PassThru] [-LookupHostname] [-DualMode] [-Default] [-Favicon <Byte[]>]
 [-DefaultFavicon] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertName
```
Add-PodeEndpoint [-Address <String>] [-Port <Int32>] [-Hostname <String>] [-Protocol <String>]
 -CertificateName <String> [-CertificateStoreName <StoreName>] [-CertificateStoreLocation <StoreLocation>]
 [-TlsMode <String>] [-Name <String>] [-RedirectTo <String>] [-Description <String>] [-Acknowledge <String>]
 [-SslProtocol <String[]>] [-CRLFMessageEnd] [-Force] [-AllowClientCertificate] [-PassThru] [-LookupHostname]
 [-DualMode] [-Default] [-Favicon <Byte[]>] [-DefaultFavicon] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### CertRaw
```
Add-PodeEndpoint [-Address <String>] [-Port <Int32>] [-Hostname <String>] [-Protocol <String>]
 -X509Certificate <X509Certificate> [-TlsMode <String>] [-Name <String>] [-RedirectTo <String>]
 [-Description <String>] [-Acknowledge <String>] [-SslProtocol <String[]>] [-CRLFMessageEnd] [-Force]
 [-AllowClientCertificate] [-PassThru] [-LookupHostname] [-DualMode] [-Default] [-Favicon <Byte[]>]
 [-DefaultFavicon] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### CertSelf
```
Add-PodeEndpoint [-Address <String>] [-Port <Int32>] [-Hostname <String>] [-Protocol <String>]
 [-TlsMode <String>] [-Name <String>] [-RedirectTo <String>] [-Description <String>] [-Acknowledge <String>]
 [-SslProtocol <String[]>] [-CRLFMessageEnd] [-Force] [-SelfSigned] [-AllowClientCertificate] [-PassThru]
 [-LookupHostname] [-DualMode] [-Default] [-Favicon <Byte[]>] [-DefaultFavicon]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Bind an endpoint to listen for incoming Requests.
The endpoints can be HTTP, HTTPS, TCP or SMTP, with the option to bind certificates.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeEndpoint -Address localhost -Port 8090 -Protocol Http
```

### EXAMPLE 2
```
Add-PodeEndpoint -Address localhost -Protocol Smtp
```

### EXAMPLE 3
```
Add-PodeEndpoint -Address dev.pode.com -Port 8443 -Protocol Https -SelfSigned
```

### EXAMPLE 4
```
Add-PodeEndpoint -Address 127.0.0.2 -Hostname dev.pode.com -Port 8443 -Protocol Https -SelfSigned
```

### EXAMPLE 5
```
Add-PodeEndpoint -Address live.pode.com -Protocol Https -CertificateThumbprint '2A9467F7D3940243D6C07DE61E7FCCE292'
```

## PARAMETERS

### -Acknowledge
An optional Acknowledge message to send to clients when they first connect, for TCP and SMTP endpoints only.

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

### -Address
The IP/Hostname of the endpoint (Default: localhost).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowClientCertificate
Allow for client certificates to be sent on requests.

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

### -Certificate
The path to a certificate that can be used to enable HTTPS.

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

### -CertificateKey
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

### -CertificateName
A certificate subject name to bind onto HTTPS endpoints (Windows).

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
Type: Object
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
A certificate thumbprint to bind onto HTTPS endpoints (Windows).

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

### -CRLFMessageEnd
If supplied, TCP endpoints will expect incoming data to end with CRLF.

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

### -Default
If supplied, this endpoint will be the default one used for internally generating URLs.

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

### -DefaultFavicon
If supplied, enable the default Pode favicon for HTTP/HTTPS endpoints.

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

### -Description
A quick description of the Endpoint - normally used in OpenAPI.

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

### -DualMode
If supplied, this endpoint will listen on both the IPv4 and IPv6 versions of the supplied -Address.
For IPv6, this will only work if the IPv6 address can convert to a valid IPv4 address.

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

### -Favicon
A byte array representing a custom favicon for HTTP/HTTPS endpoints.

```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Ignore Administrator checks for non-localhost endpoints.

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

### -Hostname
An optional hostname for the endpoint, specifying a hostname restricts access to just the hostname.

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

### -LookupHostname
If supplied, a supplied Hostname will have its IP Address looked up from host file or DNS.

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

### -Name
An optional name for the endpoint, that can be used with other functions (Default: GUID).

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

### -PassThru
If supplied, the endpoint created will be returned.

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

### -Port
The Port number of the endpoint.

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

### -Protocol
The protocol of the supplied endpoint.

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

### -RedirectTo
The Name of another Endpoint to automatically generate a redirect route for all traffic.

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

### -SelfSigned
Create and bind a self-signed certificate for HTTPS endpoints.

```yaml
Type: SwitchParameter
Parameter Sets: CertSelf
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProtocol
One or more optional SSL Protocols this endpoints supports.
(Default: what the OS support by default).

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

### -TlsMode
The TLS mode to use on secure connections, options are Implicit or Explicit (SMTP only) (Default: Implicit).

```yaml
Type: String
Parameter Sets: CertFile, CertThumb, CertName, CertRaw, CertSelf
Aliases:

Required: False
Position: Named
Default value: Implicit
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificate
The raw X509 certificate that can be used to enable HTTPS.

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

### System.Collections.Hashtable
## NOTES

## RELATED LINKS
