---
title: Get Warning Information while Saving Visio File
type: docs
weight: 110
url: /net/get-warning-information-while-saving-visio-file/
---

## **Possible Usage Scenarios**

Sometimes the user tries to save the diagram which contains text that does not have a local font. In such case, Aspose.Diagram throws warnings while saving the diagram. You can catch these warnings by implementing the **[IWarningCallback](https://apireference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** interface and setting **[SaveOptions.WarningCallback](https://apireference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)** property.

## **Get Warnings while Saving Visio File**

The following sample code explains how to get warnings while saving visio file. The code convert the [sample visio file](sampleFontSubstitution.vsdx) which throws **[FontSubstitution](https://apireference.aspose.com/diagram/net/aspose.diagram/warningtype)** warning on saving. This warning is then caught by **[IWarningCallback.Warning()](https://apireference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)** method that prints the warning messages on the console.  Please also check the console output of the code given below for more understanding.

## **Sample Code**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **Console Output**

Here is the console output of the above code when executed with the provided [sample visio file](sampleFontSubstitution.vsdx).

{{< highlight java >}}
Font substitution: Font [ Athene Logos ] has been substituted by Font[Times New Roman]
{{< /highlight >}}
