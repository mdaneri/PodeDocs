---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Authentication
schema: 2.0.0
---

# Merge-PodeAuth

## SYNOPSIS
Lets you merge multiple Authentication methods together, into a "single" Authentication method.

## SYNTAX

### ScriptBlock (Default)
```
Merge-PodeAuth -Name <String> -Authentication <String[]> [-Valid <String>] [-ScriptBlock <ScriptBlock>]
 [-Default <String>] [-FailureUrl <String>] [-FailureMessage <String>] [-SuccessUrl <String>] [-Sessionless]
 [-SuccessUseOrigin] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### MergeDefault
```
Merge-PodeAuth -Name <String> -Authentication <String[]> [-Valid <String>] [-Default <String>]
 [-MergeDefault <String>] [-FailureUrl <String>] [-FailureMessage <String>] [-SuccessUrl <String>]
 [-Sessionless] [-SuccessUseOrigin] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Lets you merge multiple Authentication methods together, into a "single" Authentication method.
You can specify if only One or All of the methods need to pass to allow access, and you can also
merge other merged Authentication methods for more advanced scenarios.

## EXAMPLES

### EXAMPLE 1
```
Merge-PodeAuth -Name MergedAuth -Authentication ApiTokenAuth, BasicAuth -Valid All -ScriptBlock { ... }
```

### EXAMPLE 2
```
Merge-PodeAuth -Name MergedAuth -Authentication ApiTokenAuth, BasicAuth -Valid All -MergeDefault BasicAuth
```

### EXAMPLE 3
```
Merge-PodeAuth -Name MergedAuth -Authentication ApiTokenAuth, BasicAuth -FailureUrl 'http://localhost:8080/login'
```

## PARAMETERS

### -Authentication
Multiple Autentication method Names to be merged.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Auth

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Default
The Default Authentication method to use as a fallback for Failure URLs and other settings.

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
This will be used as fallback for the merged Authentication methods if not set on them.

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
This will be used as fallback for the merged Authentication methods if not set on them.

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

### -MergeDefault
The Default Authentication method's User details result object to use, when $Valid=All.

```yaml
Type: String
Parameter Sets: MergeDefault
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
This is mandatory, and only used, when $Valid=All.
A scriptblock to merge the mutliple users/headers returned by valid authentications into 1 user/header objects.
This scriptblock will receive a hashtable of all result objects returned from Authentication methods.
The key for the hashtable will be the authentication names that passed.

```yaml
Type: ScriptBlock
Parameter Sets: ScriptBlock
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sessionless
If supplied, authenticated users will not be stored in sessions, and sessions will not be used.
This will be used as fallback for the merged Authentication methods if not set on them.

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
This will be used as fallback for the merged Authentication methods if not set on them.

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
This will be used as fallback for the merged Authentication methods if not set on them.

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

### -Valid
How many of the Authentication methods are required to be valid, One or All.
(Default: One)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: One
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
