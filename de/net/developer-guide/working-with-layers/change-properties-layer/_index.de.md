---
title: Ebeneneigenschaften ändern
type: docs
weight: 130
url: /de/net/change-properties-layer/
description: In diesem Abschnitt wird erläutert, wie Sie die Layer-Eigenschaften mit Aspose.Diagram ändern.
---
## **Ändern Sie die Layer-Eigenschaften in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) Ermöglicht das Ändern der Layer-Eigenschaften in Microsoft Office Visio diagram. Jede Form kann zu mehreren Layern gehören, sodass Entwickler die Layer-Eigenschaften an die Bedürfnisse des Endbenutzers anpassen können. Das[Seitenblatt](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)Das Klassenobjekt bietet Ebenen, mit denen Ebenenobjekte in Visio-Zeichnungen hinzugefügt und entfernt werden können. Benutzer können verwalten[Schicht](https://reference.aspose.com/diagram/net/aspose.diagram/layer) Eigenschaften programmgesteuert mit Aspose.Diagram API wie folgt:
### **Programmierbeispiel zum Ändern der Layer-Eigenschaften**
Der folgende Codeabschnitt hilft, die Eigenschaften der Ebene zu ändern.


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
