---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Jwt
schema: 2.0.0
---

# Test-PodeJwt

## SYNOPSIS
Validates a JWT payload by checking its registered claims as defined in RFC 7519.

## SYNTAX

```
Test-PodeJwt [-Payload] <PSObject> [[-Issuer] <String>] [[-JwtVerificationMode] <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function verifies the validity of a JWT payload by ensuring:
- The \`exp\` (Expiration Time) has not passed.
- The \`nbf\` (Not Before) time is not in the future.
- The \`iat\` (Issued At) time is not in the future.
- The \`iss\` (Issuer) claim is valid based on the verification mode.
- The \`sub\` (Subject) claim is a valid string.
- The \`aud\` (Audience) claim is valid based on the verification mode.
- The \`jti\` (JWT ID) claim is a valid string.

## EXAMPLES

### EXAMPLE 1
```
$payload = [pscustomobject]@{
    iss = "auth.example.com"
    sub = "1234567890"
    aud = "myapi.example.com"
    exp = 1700000000
    nbf = 1690000000
    iat = 1690000000
    jti = "unique-token-id"
}
```

Test-PodeJwt -Payload $payload -JwtVerificationMode "Strict"

This example validates a JWT payload with full claim verification.

## PARAMETERS

### -Issuer
The expected JWT Issuer.
If omitted, uses 'Pode'.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: Pode
Accept pipeline input: False
Accept wildcard characters: False
```

### -JwtVerificationMode
Defines how aggressively JWT claims should be checked:
- \`Strict\`: Requires all standard claims to be valid (\`exp\`, \`nbf\`, \`iat\`, \`iss\`, \`aud\`, \`jti\`).
- \`Moderate\`: Allows missing \`iss\` and \`aud\` but still checks expiration.
- \`Lenient\`: Ignores missing \`iss\` and \`aud\`, only verifies \`exp\`, \`nbf\`, and \`iat\`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Lenient
Accept pipeline input: False
Accept wildcard characters: False
```

### -Payload
The JWT payload as a \[pscustomobject\] containing registered claims such as \`exp\`, \`nbf\`, \`iat\`, \`iss\`, \`sub\`, \`aud\`, and \`jti\`.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

## NOTES

## RELATED LINKS
