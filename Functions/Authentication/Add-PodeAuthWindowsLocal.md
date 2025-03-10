---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Add-PodeAuthWindowsLocal

## SYNOPSIS
Adds the inbuilt Windows Local User Authentication method for verifying users.

## SYNTAX

### Groups (Default)
```
Add-PodeAuthWindowsLocal -Name <String> -Scheme <Hashtable> [-Groups <String[]>] [-Users <String[]>]
 [-FailureUrl <String>] [-FailureMessage <String>] [-SuccessUrl <String>] [-ScriptBlock <ScriptBlock>]
 [-Sessionless] [-SuccessUseOrigin] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### NoGroups
```
Add-PodeAuthWindowsLocal -Name <String> -Scheme <Hashtable> [-Users <String[]>] [-FailureUrl <String>]
 [-FailureMessage <String>] [-SuccessUrl <String>] [-ScriptBlock <ScriptBlock>] [-Sessionless] [-NoGroups]
 [-SuccessUseOrigin] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds the inbuilt Windows Local User Authentication method for verifying users.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAuthScheme -Form | Add-PodeAuthWindowsLocal -Name 'WinAuth'
```

### EXAMPLE 2
```
New-PodeAuthScheme -Basic | Add-PodeAuthWindowsLocal -Name 'WinAuth' -Groups @('Developers')
```

### EXAMPLE 3
```
New-PodeAuthScheme -Form | Add-PodeAuthWindowsLocal -Name 'WinAuth' -NoGroups
```

## PARAMETERS

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
If supplied, groups will not be retrieved for the user.

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
