---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# New-PodeAccessScheme

## SYNOPSIS
Create a new type of Access scheme.

## SYNTAX

### Type_Path (Default)
```
New-PodeAccessScheme -Type <String> [-Path <String>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Type_Scriptblock
```
New-PodeAccessScheme -Type <String> [-ScriptBlock <ScriptBlock>] [-ArgumentList <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Custom_Path
```
New-PodeAccessScheme [-Custom] -Path <String> [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Custom_Scriptblock
```
New-PodeAccessScheme [-Custom] -ScriptBlock <ScriptBlock> [-ArgumentList <Object[]>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Create a new type of Access scheme, which retrieves the destination/resource's authorisation values which a user needs for access.

## EXAMPLES

### EXAMPLE 1
```
$role_access = New-PodeAccessScheme -Type Role
```

### EXAMPLE 2
```
$group_access = New-PodeAccessScheme -Type Group -Path 'Metadata.Groups'
```

### EXAMPLE 3
```
$scope_access = New-PodeAccessScheme -Type Scope -Scriptblock { param($user) return @(Get-ExampleAccess -Username $user.Username) }
```

### EXAMPLE 4
```
$custom_access = New-PodeAccessScheme -Custom -Path 'CustomProp'
```

## PARAMETERS

### -ArgumentList
An optional array of arguments to supply to the ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: Type_Scriptblock, Custom_Scriptblock
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Custom
If supplied, the access Scheme will be flagged as using Custom logic.

```yaml
Type: SwitchParameter
Parameter Sets: Custom_Path, Custom_Scriptblock
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
An optional property Path within the $WebEvent.Auth.User object to extract authorisation values.
The default Path is based on the Access Type, either Roles; Groups; Scopes; or Username.
This, or ScriptBlock, is mandatory if using a Custom scheme.

```yaml
Type: String
Parameter Sets: Type_Path
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Custom_Path
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
An optional ScriptBlock for retrieving authorisation values for the authenticated user, useful if the values reside in an external data store.
This, or Path, is mandatory if using a Custom scheme.

```yaml
Type: ScriptBlock
Parameter Sets: Type_Scriptblock
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ScriptBlock
Parameter Sets: Custom_Scriptblock
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
The inbuilt Type of Access this method is for: Role, Group, Scope, User.

```yaml
Type: String
Parameter Sets: Type_Path, Type_Scriptblock
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Hashtable
## NOTES

## RELATED LINKS
