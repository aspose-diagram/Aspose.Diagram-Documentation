+++
title = "Retrieving Font Information" 
description = "" 
weight = 16102 
+++

Aspose.Diagram for .NET : Retrieving Font Information  

# Aspose.Diagram for .NET : Retrieving Font Information


## VSTO

Below is the code for retrieving font information:

{{< code lang="cs" >}}
 foreach (Font font in Application.ActiveDocument.Fonts)
 {
    //Display information about the fonts
    MessageBox.Show(font.Name);
 }
{{< /code >}}

## Aspose.Diagram

Aspose.Diagram has mechanisms for retrieving information about the elements that make up a diagram, from [pages](/pages/createpage.action?spaceKey=diagramnet&title=Retrieving+Page+Information&linkCreation=true&fromPageId=18354903), [stencils](/pages/createpage.action?spaceKey=diagramnet&title=Retrieving+Master+Information&linkCreation=true&fromPageId=18354903), [connectors](https://docs2.aspose.com/diagram/net/plugins/asposediagramnetforvsto/codecomparisonforcommonfeatures/retrieving+connector+information) and also fonts. This article shows how to find out which fonts are used in a diagram.

The [`Font`](/pages/createpage.action?spaceKey=diagramnet&title=Font+Class&linkCreation=true&fromPageId=18354903) object represents a typeface that is either applied to text in a document or available for use on the system.

A `Font` object maps a name (for example, "Arial") to the font ID (for example, 3) that Microsoft Visio stores in a `Font` cell in a `Character` section of a shape that contains text formatted with that font. Font IDs can change when a document is opened on different systems or when fonts are installed or removed.

{{< code lang="cs" >}}
 //Call the diagram constructor to load diagram from a VDX file
 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)
 {
    //Display information about the fonts
    Console.WriteLine(font.Name);
 }
{{< /code >}}

## Download Sample Code

*   [Codeplex](https://asposevsto.codeplex.com/releases/view/617141)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932)

## Download Running Code

*   [Codeplex](https://asposevsto.codeplex.com/SourceControl/latest#Aspose.Diagram Vs VSTO Visio/Retrieving Font Information/)
*   [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
*   [Code.MSDN](https://code.msdn.microsoft.com/AsposeDiagram-Vs-VSTO-fb086932/view/SourceCode#content)

