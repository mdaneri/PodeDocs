---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Core
schema: 2.0.0
---

# Start-PodeStaticServer

## SYNOPSIS
Helper wrapper function to start a Pode web server for a static website at the current directory.

## SYNTAX

```
Start-PodeStaticServer [[-Threads] <Int32>] [[-RootPath] <String>] [[-Address] <String>] [[-Port] <Int32>]
 [-Https] [[-Certificate] <String>] [[-CertificatePassword] <String>] [[-CertificateKey] <String>]
 [[-X509Certificate] <X509Certificate>] [[-Path] <String>] [[-Defaults] <String[]>] [-DownloadOnly]
 [-FileBrowser] [-Browse] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Helper wrapper function to start a Pode web server for a static website at the current directory.

## EXAMPLES

### EXAMPLE 1
```
Start-PodeStaticServer
```

### EXAMPLE 2
```
Start-PodeStaticServer -Address '127.0.0.3' -Port 8000
```

### EXAMPLE 3
```
Start-PodeStaticServer -Path '/installers' -DownloadOnly
```

## PARAMETERS

### -Address
The IP/Hostname of the endpoint.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -Browse
Open the web server's default endpoint in your default browser.

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
The path to a certificate that can be use to enable HTTPS.

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

### -CertificateKey
A key file to be paired with a PEM certificate referenced in CertificateFile

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

### -CertificatePassword
The password for the certificate referenced in CertificateFile.

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

### -Defaults
An array of default pages to display, such as 'index.html'.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DownloadOnly
When supplied, all static content on this Route will be attached as downloads - rather than rendered.

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

### -FileBrowser
When supplied, If the path is a folder, instead of returning 404, will return A browsable content of the directory.

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

### -Https
Start the server using HTTPS, if no certificate details are supplied a self-signed certificate will be generated.

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

### -Path
The URI path for the static Route.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: /
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
Position: 4
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

### -RootPath
An override for the Server's root path.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: $PWD
Accept pipeline input: False
Accept wildcard characters: False
```

### -Threads
The numbers of threads to use for requests.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: 3
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificate
The raw X509 certificate that can be use to enable HTTPS.

```yaml
Type: X509Certificate
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
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
