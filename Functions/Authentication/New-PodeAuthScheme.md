---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# New-PodeAuthScheme

## SYNOPSIS
Create a new type of Authentication scheme.

## SYNTAX

### Basic (Default)
```
New-PodeAuthScheme [-Basic] [-Encoding <String>] [-HeaderTag <String>] [-Description <String>]
 [-Realm <String>] [-Middleware <Object[]>] [-InnerScheme <Hashtable>] [-AsCredential]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Digest
```
New-PodeAuthScheme [-HeaderTag <String>] [-Description <String>] [-Realm <String>] [-Middleware <Object[]>]
 [-Digest] [-InnerScheme <Hashtable>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Bearer
```
New-PodeAuthScheme [-HeaderTag <String>] [-Description <String>] [-Realm <String>] [-Middleware <Object[]>]
 [-Bearer] [-Scope <String[]>] [-InnerScheme <Hashtable>] [-AsJWT] [-Secret <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Form
```
New-PodeAuthScheme [-Form] [-UsernameField <String>] [-PasswordField <String>] [-Description <String>]
 [-Realm <String>] [-Middleware <Object[]>] [-InnerScheme <Hashtable>] [-AsCredential]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Custom
```
New-PodeAuthScheme [-Custom] -ScriptBlock <ScriptBlock> [-ArgumentList <Hashtable>] [-Name <String>]
 [-Description <String>] [-Realm <String>] [-Type <String>] [-Middleware <Object[]>]
 [-PostValidator <ScriptBlock>] [-InnerScheme <Hashtable>] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### ApiKey
```
New-PodeAuthScheme [-Description <String>] [-Realm <String>] [-Middleware <Object[]>] [-ApiKey]
 [-Location <String>] [-LocationName <String>] [-InnerScheme <Hashtable>] [-AsJWT] [-Secret <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### OAuth2
```
New-PodeAuthScheme [-Description <String>] [-Realm <String>] [-Middleware <Object[]>] -ClientId <String>
 [-ClientSecret <String>] [-RedirectUrl <String>] [-AuthoriseUrl <String>] -TokenUrl <String>
 [-UserUrl <String>] [-UserUrlMethod <String>] [-CodeChallengeMethod <String>] [-UsePKCE] [-OAuth2]
 [-Scope <String[]>] [-InnerScheme <Hashtable>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ClientCertificate
```
New-PodeAuthScheme [-Description <String>] [-Realm <String>] [-Middleware <Object[]>] [-ClientCertificate]
 [-InnerScheme <Hashtable>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Negotiate
```
New-PodeAuthScheme [-Description <String>] [-Middleware <Object[]>] [-InnerScheme <Hashtable>] [-Negotiate]
 -KeytabPath <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Create a new type of Authentication scheme, which is used to parse the Request for user credentials for validating.

## EXAMPLES

### EXAMPLE 1
```
$basic_auth = New-PodeAuthScheme -Basic
```

### EXAMPLE 2
```
$form_auth = New-PodeAuthScheme -Form -UsernameField 'Email'
```

### EXAMPLE 3
```
$custom_auth = New-PodeAuthScheme -Custom -ScriptBlock { /* logic */ }
```

## PARAMETERS

### -ApiKey
If supplied, will use the inbuilt API key Authentication scheme.

```yaml
Type: SwitchParameter
Parameter Sets: ApiKey
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArgumentList
An array of arguments to supply to the Custom Authentication type's ScriptBlock.

```yaml
Type: Hashtable
Parameter Sets: Custom
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsCredential
If supplied, username/password credentials for Basic/Form authentication will instead be supplied as a pscredential object.

```yaml
Type: SwitchParameter
Parameter Sets: Basic, Form
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJWT
If supplied, the token/key supplied for Bearer/API key authentication will be parsed as a JWT, and the payload supplied instead.

```yaml
Type: SwitchParameter
Parameter Sets: Bearer, ApiKey
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthoriseUrl
The OAuth2 Authorisation URL to authenticate a User.
This is optional if you're using an InnerScheme like Basic/Form.

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Basic
If supplied, will use the inbuilt Basic Authentication credentials retriever.

```yaml
Type: SwitchParameter
Parameter Sets: Basic
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bearer
If supplied, will use the inbuilt Bearer Authentication token retriever.

```yaml
Type: SwitchParameter
Parameter Sets: Bearer
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientCertificate
If supplied, will use the inbuilt Client Certificate Authentication scheme.

```yaml
Type: SwitchParameter
Parameter Sets: ClientCertificate
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientId
The Application ID generated when registering a new app for OAuth2.

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientSecret
The Application Secret generated when registering a new app for OAuth2 (this is optional when using PKCE).

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CodeChallengeMethod
An optional method for sending a PKCE code challenge when calling the Authorise URL - for OAuth2 (Default: S256)

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: S256
Accept pipeline input: False
Accept wildcard characters: False
```

### -Custom
If supplied, will allow you to create a Custom Authentication credentials retriever.

```yaml
Type: SwitchParameter
Parameter Sets: Custom
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A short description for security scheme.
CommonMark syntax MAY be used for rich text representation

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

### -Digest
If supplied, will use the inbuilt Digest Authentication credentials retriever.

```yaml
Type: SwitchParameter
Parameter Sets: Digest
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Encoding
The Encoding to use when decoding the Basic Authorization header.

```yaml
Type: String
Parameter Sets: Basic
Aliases:

Required: False
Position: Named
Default value: ISO-8859-1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Form
If supplied, will use the inbuilt Form Authentication credentials retriever.

```yaml
Type: SwitchParameter
Parameter Sets: Form
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeaderTag
The Tag name used in the Authorization header, ie: Basic, Bearer, Digest.

```yaml
Type: String
Parameter Sets: Basic, Digest, Bearer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InnerScheme
An optional authentication Scheme (from New-PodeAuthScheme) that will be called prior to this Scheme.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeytabPath
The path to the Keytab file for Negotiate authentication.

```yaml
Type: String
Parameter Sets: Negotiate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
The Location to find an API key: Header, Query, or Cookie.
(Default: Header)

```yaml
Type: String
Parameter Sets: ApiKey
Aliases:

Required: False
Position: Named
Default value: Header
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocationName
The Name of the Header, Query, or Cookie to find an API key.
(Default depends on Location.
Header/Cookie: X-API-KEY, Query: api_key)

```yaml
Type: String
Parameter Sets: ApiKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Middleware
An array of ScriptBlocks for optional Middleware to run before the Scheme's scriptblock.

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

### -Name
The Name of an Authentication type - such as Basic or NTLM.

```yaml
Type: String
Parameter Sets: Custom
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Negotiate
If supplied, will use the inbuilt Negotiate Authentication scheme (Kerberos/NTLM).

```yaml
Type: SwitchParameter
Parameter Sets: Negotiate
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OAuth2
If supplied, will use the inbuilt OAuth2 Authentication scheme.

```yaml
Type: SwitchParameter
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordField
The name of the Password Field in the payload to retrieve the password.

```yaml
Type: String
Parameter Sets: Form
Aliases:

Required: False
Position: Named
Default value: Password
Accept pipeline input: False
Accept wildcard characters: False
```

### -PostValidator
The PostValidator is a scriptblock that is invoked after user validation.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
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

### -Realm
The name of scope of the protected area.

```yaml
Type: String
Parameter Sets: Basic, Digest, Bearer, Form, Custom, ApiKey, OAuth2, ClientCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectUrl
An optional OAuth2 Redirect URL (default: \<host\>/oauth2/callback)

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
An optional array of Scopes for Bearer/OAuth2 Authentication.
(These are case-sensitive)

```yaml
Type: String[]
Parameter Sets: Bearer, OAuth2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptBlock
The ScriptBlock is used to parse the request and retieve user credentials and other information.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Secret
An optional Secret, used to sign/verify JWT signatures.

```yaml
Type: String
Parameter Sets: Bearer, ApiKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TokenUrl
The OAuth2 Token URL to acquire an access token.

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
The scheme type for custom Authentication types.
Default is HTTP.

```yaml
Type: String
Parameter Sets: Custom
Aliases:

Required: False
Position: Named
Default value: Http
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePKCE
If supplied, OAuth2 authentication will use PKCE code verifiers - for OAuth2

```yaml
Type: SwitchParameter
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsernameField
The name of the Username Field in the payload to retrieve the username.

```yaml
Type: String
Parameter Sets: Form
Aliases:

Required: False
Position: Named
Default value: Username
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserUrl
An optional User profile URL to retrieve a user's details - for OAuth2

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserUrlMethod
An optional HTTP method to use when calling the User profile URL - for OAuth2 (Default: Post)

```yaml
Type: String
Parameter Sets: OAuth2
Aliases:

Required: False
Position: Named
Default value: Post
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
