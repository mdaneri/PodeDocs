---
external help file: Pode-help.xml
Module Name: Pode
online version:
PodeType: Utilities
schema: 2.0.0
---

# ConvertFrom-PodeXml

## SYNOPSIS
Converts an XML node to a PowerShell hashtable.

## SYNTAX

```
ConvertFrom-PodeXml [-node] <XmlNode> [-Prefix <String>] [-ShowDocElement] [-KeepAttributes]
 [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
The ConvertFrom-PodeXml function converts an XML node, including all its child nodes and attributes, into an ordered hashtable.
This is useful for manipulating XML data in a more PowerShell-centric way.

## EXAMPLES

### EXAMPLE 1
```
$node = [xml](Get-Content 'path\to\file.xml').DocumentElement
ConvertFrom-PodeXml -node $node
```

Converts the XML document's root node to a hashtable.

## PARAMETERS

### -KeepAttributes
If set, the function keeps the attributes of the XML nodes in the resulting hashtable.

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

### -node
The XML node to convert.
This parameter takes an XML node and processes it, along with its child nodes and attributes.

```yaml
Type: XmlNode
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Prefix
A string prefix used to indicate an attribute.
Default is an empty string.

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

### -ShowDocElement
Indicates whether to show the document element.
Default is false.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Xml.XmlNode
### You can pipe a XmlNode to ConvertFrom-PodeXml.
## OUTPUTS

### System.Collections.Hashtable
### Outputs an ordered hashtable representing the XML node structure.
## NOTES
This cmdlet is useful for transforming XML data into a structure that's easier to manipulate in PowerShell scripts.

## RELATED LINKS
