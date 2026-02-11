---
title: Formdaten aktualisieren
type: docs
weight: 40
url: /de/net/refresh-shapes-data/
description: In diesem Abschnitt wird erläutert, wie Sie die Shape-Daten für ein visio-Shape mit Aspose.Diagram aktualisieren.
---
## **Aktualisiert die Position der Form, einschließlich xform, Verbindung und Geom, wenn der Text der Form oder anderer geändert wird**
 Die RefreshData-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse kann verwendet werden, um die Daten der Form zu aktualisieren

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Aktualisieren Sie die Daten der Form.
### **Aktualisieren Sie die Daten von Shape**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um eine Form mit Aspose.Diagram for .NET zu aktualisieren.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


