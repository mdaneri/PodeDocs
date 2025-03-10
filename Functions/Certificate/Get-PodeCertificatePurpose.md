---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Certificate
schema: 2.0.0
---

# Get-PodeCertificatePurpose

## SYNOPSIS
Retrieves the Enhanced Key Usage (EKU) purposes of an X.509 certificate.

## SYNTAX

```
Get-PodeCertificatePurpose [-Certificate] <X509Certificate2> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
This internal function extracts the Enhanced Key Usage (EKU) extension (OID: 2.5.29.37)
from an X.509 certificate and returns the recognized purposes.

If the certificate has no EKU extension, an empty array is returned, indicating
that the certificate has no usage restrictions.

## EXAMPLES

### EXAMPLE 1
```
$purposes = Get-PodeCertificatePurpose -Certificate $cert
Retrieves the list of EKU purposes assigned to the given certificate.
```

## PARAMETERS

### -Certificate
The X509Certificate2 object from which to retrieve the EKU purposes.

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

### [object[]]
### Returns an array of recognized EKU purposes. Supported values:
###   - 'ServerAuth'      (1.3.6.1.5.5.7.3.1)
###   - 'ClientAuth'      (1.3.6.1.5.5.7.3.2)
###   - 'CodeSigning'     (1.3.6.1.5.5.7.3.3)
###   - 'EmailSecurity'   (1.3.6.1.5.5.7.3.4)
### If an unrecognized EKU OID is found, it is returned as `"Unknown (<OID>)"`.
### If no EKU extension is present, an empty array is returned.
## NOTES

## RELATED LINKS
