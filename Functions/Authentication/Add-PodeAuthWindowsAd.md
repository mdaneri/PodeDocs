---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Add-PodeAuthWindowsAd

## SYNOPSIS
Adds the inbuilt Windows AD Authentication method for verifying users.

## SYNTAX

### Groups (Default)
```
Add-PodeAuthWindowsAd -Name <String> -Scheme <Hashtable> [-Fqdn <String>] [-Domain <String>]
 [-SearchBase <String>] [-Groups <String[]>] [-Users <String[]>] [-FailureUrl <String>]
 [-FailureMessage <String>] [-SuccessUrl <String>] [-ScriptBlock <ScriptBlock>] [-Sessionless] [-DirectGroups]
 [-OpenLDAP] [-ADModule] [-SuccessUseOrigin] [-KeepCredential] [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

### NoGroups
```
Add-PodeAuthWindowsAd -Name <String> -Scheme <Hashtable> [-Fqdn <String>] [-Domain <String>]
 [-SearchBase <String>] [-Users <String[]>] [-FailureUrl <String>] [-FailureMessage <String>]
 [-SuccessUrl <String>] [-ScriptBlock <ScriptBlock>] [-Sessionless] [-NoGroups] [-OpenLDAP] [-ADModule]
 [-SuccessUseOrigin] [-KeepCredential] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds the inbuilt Windows AD Authentication method for verifying users.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAuthScheme -Form | Add-PodeAuthWindowsAd -Name 'WinAuth'
```

### EXAMPLE 2
```
New-PodeAuthScheme -Basic | Add-PodeAuthWindowsAd -Name 'WinAuth' -Groups @('Developers')
```

### EXAMPLE 3
```
New-PodeAuthScheme -Form | Add-PodeAuthWindowsAd -Name 'WinAuth' -NoGroups
```

### EXAMPLE 4
```
New-PodeAuthScheme -Form | Add-PodeAuthWindowsAd -Name 'UnixAuth' -Server 'testdomain.company.com' -Domain 'testdomain'
```

## PARAMETERS

### -ADModule
If supplied, and on Windows, the ActiveDirectory module will be used instead.

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

### -DirectGroups
If supplied, only a user's direct groups will be retrieved rather than all groups recursively.

```yaml
Type: SwitchParameter
Parameter Sets: Groups
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain
(Unix Only) A custom NetBIOS domain name that is prepended onto usernames that are missing it (\<Domain\>\\\<Username\>).

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

### -FailureMessage
An override Message to throw when authentication fails.

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

### -FailureUrl
The URL to redirect to when authentication fails.

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

### -Fqdn
A custom FQDN for the DNS of the AD you wish to authenticate against.
(Alias: Server)

```yaml
Type: String
Parameter Sets: (All)
Aliases: Server

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Groups
An array of Group names to only allow access.

```yaml
Type: String[]
Parameter Sets: Groups
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeepCredential
If suplied pode will save the AD credential as a PSCredential object in $WebEvent.Auth.User.Credential

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
A unique Name for the Authentication method.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoGroups
If supplied, groups will not be retrieved for the user in AD.

```yaml
Type: SwitchParameter
Parameter Sets: NoGroups
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OpenLDAP
If supplied, and on Windows, OpenLDAP will be used instead (this is the default for Linux/MacOS).

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

### -Scheme
The Scheme to use for retrieving credentials (From New-PodeAuthScheme).

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ScriptBlock
Optional ScriptBlock that is passed the found user object for further validation.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchBase
(Unix Only) An optional searchbase to refine the LDAP query.
This should be the full distinguished name.

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

### -Sessionless
If supplied, authenticated users will not be stored in sessions, and sessions will not be used.

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

### -SuccessUrl
The URL to redirect to when authentication succeeds when logging in.

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

### -SuccessUseOrigin
If supplied, successful authentication from a login page will redirect back to the originating page instead of the FailureUrl.

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

### -Users
An array of Usernames to only allow access.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
