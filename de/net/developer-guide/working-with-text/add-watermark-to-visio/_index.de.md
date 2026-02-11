---
title: Wasserzeichen zu Visio hinzufügen
type: docs
weight: 10
url: /de/net/add-watermark-to-visio/
keywords: watermark, visi
description: So fügen Sie visio ein Wasserzeichen hinzu, indem Sie .NET Diagram API verwenden.
---
## **Erstellen einer Diagram**
 Mit Aspose.Diagram for .NET können Sie Microsoft Visio Diagramme aus Ihren eigenen Anwendungen lesen und erstellen, ohne Microsoft Office Automatisierung. Der erste Schritt beim Erstellen neuer Dokumente ist das Erstellen einer diagram. Dann[Fügen Sie Formen und Verbinder hinzu](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)um die diagram aufzubauen. Verwenden Sie den Standardkonstruktor von[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, um eine neue diagram zu erstellen.
### **Programmierbeispiel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Wasserzeichen zu visio auf der Seite hinzufügen
1. Rufen Sie die Save-Methode des Klassenobjekts Diagram auf und übergeben Sie auch den vollständigen Dateipfad und das DiagramSaveOptions-Objekt.
### **Programmierbeispiel für Wasserzeichen hinzufügen**
Der folgende Beispielcode zeigt, wie man Wasserzeichen in Visio diagram hinzufügt.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    double pinx = page.PageSheet.PageProps.PageWidth.Value / 2;
    double piny = page.PageSheet.PageProps.PageHeight.Value / 2;
    double width = page.PageSheet.PageProps.PageWidth.Value;
    double height = page.PageSheet.PageProps.PageHeight.Value;
    
    //Add watermark
    Shape shape = page.AddText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);
    diagram.Save(dataDir + "Watermark.vsdx", SaveFileFormat.VSDX);
}


{{< /highlight >}}
```
