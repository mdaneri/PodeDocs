---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Security
schema: 2.0.0
---

# Add-PodeSecurityPermissionsPolicy

## SYNOPSIS
Adds additional values to already defined values for the Permissions-Policy header.

## SYNTAX

```
Add-PodeSecurityPermissionsPolicy [[-Accelerometer] <String[]>] [[-AmbientLightSensor] <String[]>]
 [[-Autoplay] <String[]>] [[-Battery] <String[]>] [[-Camera] <String[]>] [[-DisplayCapture] <String[]>]
 [[-DocumentDomain] <String[]>] [[-EncryptedMedia] <String[]>] [[-Fullscreen] <String[]>]
 [[-Gamepad] <String[]>] [[-Geolocation] <String[]>] [[-Gyroscope] <String[]>] [[-InterestCohort] <String[]>]
 [[-LayoutAnimations] <String[]>] [[-LegacyImageFormats] <String[]>] [[-Magnetometer] <String[]>]
 [[-Microphone] <String[]>] [[-Midi] <String[]>] [[-OversizedImages] <String[]>] [[-Payment] <String[]>]
 [[-PictureInPicture] <String[]>] [[-PublicKeyCredentials] <String[]>] [[-Speakers] <String[]>]
 [[-SyncXhr] <String[]>] [[-UnoptimisedImages] <String[]>] [[-UnsizedMedia] <String[]>] [[-Usb] <String[]>]
 [[-ScreenWakeLake] <String[]>] [[-WebShare] <String[]>] [[-XrSpatialTracking] <String[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds additional values to already defined values for the Permissions-Policy header, instead of overriding them.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeSecurityPermissionsPolicy -AmbientLightSensor 'none'
```

## PARAMETERS

### -Accelerometer
The values to add for the Accelerometer portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AmbientLightSensor
The values to add for the AmbientLightSensor portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Autoplay
The values to add for the Autoplay portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Battery
The values to add for the Battery portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Camera
The values to add for the Camera portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayCapture
The values to add for the DisplayCapture portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentDomain
The values to add for the DocumentDomain portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptedMedia
The values to add for the EncryptedMedia portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fullscreen
The values to add for the Fullscreen portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gamepad
The values to add for the Gamepad portion of the header.

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

### -Geolocation
The values to add for the Geolocation portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gyroscope
The values to add for the Gyroscope portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterestCohort
The values to use for the InterestCohort portal of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LayoutAnimations
The values to add for the LayoutAnimations portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyImageFormats
The values to add for the LegacyImageFormats portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Magnetometer
The values to add for the Magnetometer portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 16
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Microphone
The values to add for the Microphone portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Midi
The values to add for the Midi portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 18
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OversizedImages
The values to add for the OversizedImages portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 19
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Payment
The values to add for the Payment portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 20
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PictureInPicture
The values to add for the PictureInPicture portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
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

### -PublicKeyCredentials
The values to add for the PublicKeyCredentials portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScreenWakeLake
The values to add for the ScreenWakeLake portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 28
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Speakers
The values to add for the Speakers portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 23
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncXhr
The values to add for the SyncXhr portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 24
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnoptimisedImages
The values to add for the UnoptimisedImages portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 25
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnsizedMedia
The values to add for the UnsizedMedia portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 26
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Usb
The values to add for the Usb portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 27
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebShare
The values to add for the WebShare portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 29
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XrSpatialTracking
The values to add for the XrSpatialTracking portion of the header.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 30
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
