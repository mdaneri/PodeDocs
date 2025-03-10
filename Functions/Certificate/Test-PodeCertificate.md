---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Certificate
schema: 2.0.0
---

# Test-PodeCertificate

## SYNOPSIS
Validates an X.509 certificate for both general validity and intended usage.

## SYNTAX

```
Test-PodeCertificate [-Certificate] <X509Certificate2> [-CheckRevocation] [-OfflineRevocation]
 [-AllowWeakAlgorithms] [-DenySelfSigned] [[-ExpectedPurpose] <String>] [-Strict]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
This function performs comprehensive validation on an X.509 certificate.
It checks:
  - That the certificate's validity period (NotBefore and NotAfter) is current.
  - That the certificate chain is valid (including optional revocation checking).
  - That the certificate meets security criteria (e.g.
not using weak algorithms).
  - Optionally, that the certificate's Enhanced Key Usage (EKU) includes the expected purpose.

New parameters:
  - **ExpectedPurpose**: When provided, the function checks if the certificate's EKU includes this purpose.
    Valid values: ServerAuth, ClientAuth, CodeSigning, EmailSecurity.
  - **Strict**: When used with ExpectedPurpose, if any unknown EKU is present, validation fails.
  - **AllowWeakAlgorithms**: When specified, certificates using weak algorithms are allowed.
  - **DenySelfSigned**: When specified, self-signed certificates are rejected.

If any validation step fails, the function writes an error and returns \`$false\`.
Otherwise, it returns \`$true\`.

## EXAMPLES

### EXAMPLE 1
```
Test-PodeCertificate -Certificate $cert
Performs basic validity and chain checks on the certificate.
```

### EXAMPLE 2
```
Test-PodeCertificate -Certificate $cert -CheckRevocation
Also performs online revocation checking.
```

### EXAMPLE 3
```
Test-PodeCertificate -Certificate $cert -ExpectedPurpose CodeSigning -Strict
Validates the certificate and ensures it is explicitly intended for CodeSigning.
```

## PARAMETERS

### -AllowWeakAlgorithms
A switch that, when provided, allows certificates with weak signature algorithms.

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
The X509Certificate2 object to validate.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CheckRevocation
A switch that enables revocation checking (online or offline).

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

### -DenySelfSigned
A switch that, when provided, rejects self-signed certificates.

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

### -ExpectedPurpose
An optional string specifying the expected Enhanced Key Usage (EKU) for the certificate.
Valid values: ServerAuth, ClientAuth, CodeSigning, EmailSecurity.
  - 'ServerAuth'      (1.3.6.1.5.5.7.3.1)
  - 'ClientAuth'      (1.3.6.1.5.5.7.3.2)
  - 'CodeSigning'     (1.3.6.1.5.5.7.3.3)
  - 'EmailSecurity'   (1.3.6.1.5.5.7.3.4)

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

### -OfflineRevocation
A switch that forces revocation checking to use only cached CRLs.

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

### -Strict
A switch that, when used with ExpectedPurpose, enforces that no unknown EKUs are present.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### [boolean] Returns `$true` if the certificate passes all validation and restriction checks, otherwise `$false`.
## NOTES

## RELATED LINKS
