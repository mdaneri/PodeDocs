---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Add-PodeOAInfo

## SYNOPSIS
Creates an OpenAPI metadata.

## SYNTAX

```
Add-PodeOAInfo [[-Title] <String>] [[-Version] <String>] [[-Description] <String>] [[-TermsOfService] <String>]
 [[-LicenseName] <String>] [[-LicenseUrl] <String>] [[-ContactName] <String>] [[-ContactEmail] <String>]
 [[-ContactUrl] <String>] [[-DefinitionTag] <String>]
```

## DESCRIPTION
Creates an OpenAPI metadata like TermOfService, license and so on.
The metadata MAY be used by the clients if needed, and MAY be presented in editing or documentation generation tools for convenience.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeOAInfo -TermsOfService 'http://swagger.io/terms/' -License 'Apache 2.0' -LicenseUrl 'http://www.apache.org/licenses/LICENSE-2.0.html' -ContactName 'API Support' -ContactEmail 'apiteam@swagger.io' -ContactUrl 'http://example.com/support'
```

## PARAMETERS

### -ContactEmail
The email address of the contact person/organization.
MUST be in the format of an email address.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContactName
The identifying name of the contact person/organization.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContactUrl
The URL pointing to the contact information.
MUST be in the format of a URL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionTag
A string representing the unique tag for the API specification.
This tag helps distinguish between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A short description of the API.
CommonMark syntax MAY be used for rich text representation.
https://spec.commonmark.org/

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseName
The license name used for the API.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseUrl
A URL to the license used for the API.
MUST be in the format of a URL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TermsOfService
A URL to the Terms of Service for the API.
MUST be in the format of a URL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
The Title of the API.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
The Version of the API.
The OpenAPI Specification is versioned using Semantic Versioning 2.0.0 (semver) and follows the semver specification.
https://semver.org/spec/v2.0.0.html

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
