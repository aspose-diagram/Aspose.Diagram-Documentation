---
title: Ändra lageregenskaper
type: docs
weight: 130
url: /sv/net/change-properties-layer/
description: Det här avsnittet förklarar hur du ändrar lageregenskaper med Aspose.Diagram.
---
## **Ändra lageregenskaper i Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) tillåter att ändra lagers egenskaper i Microsoft Office Visio diagram. Varje form kan tillhöra flera lager så att utvecklare kan ändra lagrets egenskaper för att passa slutanvändarens behov. De[PageSheet](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)klassobjekt erbjuder lager som gör det möjligt att lägga till och ta bort lagerobjekt i Visio-ritning. Användare kan hantera[Lager](https://reference.aspose.com/diagram/net/aspose.diagram/layer) egenskaper programmatiskt med Aspose.Diagram API enligt följande:
### **Ändra lageregenskaper Programmeringsexempel**
Följande kodbit hjälper till att ändra lagrets egenskaper.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
