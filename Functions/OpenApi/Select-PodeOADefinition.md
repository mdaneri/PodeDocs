---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: OpenApi
schema: 2.0.0
---

# Select-PodeOADefinition

## SYNOPSIS
Select a group of OpenAPI Definions for modification.

## SYNTAX

```
Select-PodeOADefinition [[-Tag] <String[]>] [-Scriptblock] <ScriptBlock> [-ProgressAction <ActionPreference>]
 [<CommonParameters>]
```

## DESCRIPTION
Select a group of OpenAPI Definions for modification.

## EXAMPLES

### EXAMPLE 1
```
Select-PodeOADefinition -Tag 'v3', 'v3.1'  -Script {
        New-PodeOAIntProperty -Name 'id'-Format Int64 -Example 10 -Required |
            New-PodeOAIntProperty -Name 'petId' -Format Int64 -Example 198772 -Required |
            New-PodeOAIntProperty -Name 'quantity' -Format Int32 -Example 7 -Required |
            New-PodeOAStringProperty -Name 'shipDate' -Format Date-Time |
            New-PodeOAStringProperty -Name 'status' -Description 'Order Status' -Required -Example 'approved' -Enum @('placed', 'approved', 'delivered') |
            New-PodeOABoolProperty -Name 'complete' |
            New-PodeOAObjectProperty -XmlName 'order' |
            Add-PodeOAComponentSchema -Name 'Order'
```

New-PodeOAContentMediaType -ContentType 'application/json', 'application/xml' -Content 'Pet' |
    Add-PodeOAComponentRequestBody -Name 'Pet' -Description 'Pet object that needs to be added to the store'

}

## PARAMETERS

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

### -Scriptblock
The ScriptBlock that will modified the group.

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
An Array of strings representing the unique tag for the API specification.
This tag helps distinguish between different versions or types of API specifications within the application.
You can use this tag to reference the specific API documentation, schema, or version that your function interacts with.
If Tag is empty or null the default Definition is selected

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
