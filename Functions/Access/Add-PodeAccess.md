---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Access
schema: 2.0.0
---

# Add-PodeAccess

## SYNOPSIS
Add an authorisation Access method.

## SYNTAX

### Match (Default)
```
Add-PodeAccess -Name <String> [-Description <String>] -Scheme <Hashtable> [-Match <String>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### ScriptBlock
```
Add-PodeAccess -Name <String> [-Description <String>] -Scheme <Hashtable> -ScriptBlock <ScriptBlock>
 [-ArgumentList <Object[]>] [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Add an authorisation Access method for use with Authentication methods, which will authorise access to Routes.
Or they can be used independant of Authentication/Routes for custom scenarios.

## EXAMPLES

### EXAMPLE 1
```
New-PodeAccessScheme -Type Role | Add-PodeAccess -Name 'Example'
```

### EXAMPLE 2
```
New-PodeAccessScheme -Type Group -Path 'Metadata.Groups' | Add-PodeAccess -Name 'Example' -Match All
```

### EXAMPLE 3
```
New-PodeAccessScheme -Type Scope -Scriptblock { param($user) return @(Get-ExampleAccess -Username $user.Username) } | Add-PodeAccess -Name 'Example'
```

### EXAMPLE 4
```
New-PodeAccessScheme -Custom -Path 'CustomProp' | Add-PodeAccess -Name 'Example' -ScriptBlock { param($userAccess, $customAccess) return $userAccess.Country -ieq $customAccess.Country }
```

## PARAMETERS

### -ArgumentList
An optional array of arguments to supply to the ScriptBlock.

```yaml
Type: Object[]
Parameter Sets: ScriptBlock
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
A short description used by OpenAPI.

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

### -Match
An optional inbuilt Match method to use when verifying access to a Route, this only applies when no custom Validator scriptblock is supplied.
(Default: One)
"One" will allow access if the User has at least one of the Route's access values.
"All" will allow access only if the User has all the values.
"None" will allow access only if the User has none of the values.

```yaml
Type: String
Parameter Sets: Match
Aliases:

Required: False
Position: Named
Default value: One
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A unique Name for the Access method.

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

### -Scheme
The access Scheme to use for retrieving credentials (From New-PodeAccessScheme).

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
An optional Scriptblock, which can be used to invoke custom validation logic to verify authorisation.

```yaml
Type: ScriptBlock
Parameter Sets: ScriptBlock
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

## NOTES

## RELATED LINKS
