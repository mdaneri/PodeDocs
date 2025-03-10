---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Add-PodeAuthIIS

## SYNOPSIS
Adds the inbuilt IIS Authentication method for verifying users passed to Pode from IIS.

## SYNTAX

### Groups (Default)
```
Add-PodeAuthIIS -Name <String> [-Groups <String[]>] [-Users <String[]>] [-FailureUrl <String>]
 [-FailureMessage <String>] [-SuccessUrl <String>] [-ScriptBlock <ScriptBlock>] [-Middleware <Object[]>]
 [-Sessionless] [-DirectGroups] [-ADModule] [-NoLocalCheck] [-SuccessUseOrigin]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### NoGroups
```
Add-PodeAuthIIS -Name <String> [-Users <String[]>] [-FailureUrl <String>] [-FailureMessage <String>]
 [-SuccessUrl <String>] [-ScriptBlock <ScriptBlock>] [-Middleware <Object[]>] [-Sessionless] [-NoGroups]
 [-ADModule] [-NoLocalCheck] [-SuccessUseOrigin] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Adds the inbuilt IIS Authentication method for verifying users passed to Pode from IIS.

## EXAMPLES

### EXAMPLE 1
```
Add-PodeAuthIIS -Name 'IISAuth'
```

### EXAMPLE 2
```
Add-PodeAuthIIS -Name 'IISAuth' -Groups @('Developers')
```

### EXAMPLE 3
```
Add-PodeAuthIIS -Name 'IISAuth' -NoGroups
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

### -NoLocalCheck
If supplied, Pode will not at attempt to retrieve local User/Group information for the authenticated user.

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
