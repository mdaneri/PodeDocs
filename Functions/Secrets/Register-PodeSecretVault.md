---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Secrets
schema: 2.0.0
---

# Register-PodeSecretVault

## SYNOPSIS
Register a Secret Vault.

## SYNTAX

### SecretManagement
```
Register-PodeSecretVault -Name <String> [-VaultParameters <Hashtable>] [-UnlockSecret <String>]
 [-UnlockSecureSecret <SecureString>] [-UnlockInterval <Int32>] [-NoUnlock] [-CacheTtl <Int32>]
 [-InitScriptBlock <ScriptBlock>] [-VaultName <String>] -ModuleName <String>
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

### Custom
```
Register-PodeSecretVault -Name <String> [-VaultParameters <Hashtable>] [-UnlockSecret <String>]
 [-UnlockSecureSecret <SecureString>] [-UnlockInterval <Int32>] [-NoUnlock] [-CacheTtl <Int32>]
 [-InitScriptBlock <ScriptBlock>] -ScriptBlock <ScriptBlock> [-UnlockScriptBlock <ScriptBlock>]
 [-RemoveScriptBlock <ScriptBlock>] [-SetScriptBlock <ScriptBlock>] [-UnregisterScriptBlock <ScriptBlock>]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Register a Secret Vault, which is defined by either custom logic or using the SecretManagement module.

## EXAMPLES

### EXAMPLE 1
```
Register-PodeSecretVault -Name 'VaultName' -ModuleName 'Az.KeyVault' -VaultParameters @{ AZKVaultName = $name; SubscriptionId = $subId }
```

### EXAMPLE 2
```
Register-PodeSecretVault -Name 'VaultName' -VaultParameters @{ Address = 'http://127.0.0.1:8200' } -ScriptBlock { ... }
```

## PARAMETERS

### -CacheTtl
An optional number of minutes that Secrets should be cached for.
(Default: 0)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitScriptBlock
An optional scriptblock to run before the Secret Vault is registered, letting you initialise any connection, contexts, etc.

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

### -ModuleName
For SecretManagement module Secret Vaults, this is the name/path of the extension module to be used.

```yaml
Type: String
Parameter Sets: SecretManagement
Aliases: Module

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
The unique friendly Name of the Secret Vault within Pode.

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

### -NoUnlock
If supplied, the Secret Vault will not be unlocked after registration.
To unlock you'll need to call Unlock-PodeSecretVault.

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

### -RemoveScriptBlock
For custom Secret Vaults, this is an optional scriptblock used to remove a Secret from the Vault.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
Aliases: Remove

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptBlock
For custom Secret Vaults, this is a scriptblock used to read the Secret from the Vault.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetScriptBlock
For custom Secret Vaults, this is an optional scriptblock used to create/update a Secret in the Vault.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
Aliases: Set

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnlockInterval
An optional number of minutes that Pode will periodically check/unlock the Secret Vault.
(Default: 0)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnlockScriptBlock
For custom Secret Vaults, this is an optional scriptblock used to unlock the Secret Vault.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
Aliases: Unlock

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnlockSecret
An optional Secret to be used to unlock the Secret Vault if need.

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

### -UnlockSecureSecret
An optional Secret, as a SecureString, to be used to unlock the Secret Vault if need.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnregisterScriptBlock
For custom Secret Vaults, this is an optional scriptblock used unregister the Secret Vault with any custom clean-up logic.

```yaml
Type: ScriptBlock
Parameter Sets: Custom
Aliases: Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
For SecretManagement module Secret Vaults, you can use thie parameter to specify the actual Vault name, and use the above Name parameter as a more friendly name if required.

```yaml
Type: String
Parameter Sets: SecretManagement
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultParameters
A hashtable of extra parameters that should be supplied to either the SecretManagement module, or custom scriptblocks.

```yaml
Type: Hashtable
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
