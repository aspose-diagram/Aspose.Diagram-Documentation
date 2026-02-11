---
title: Wasserzeichen zu Visio hinzufügen
type: docs
weight: 10
url: /de/java/add-watermark-to-visio/
keywords: watermark, visi
description: So fügen Sie visio ein Wasserzeichen hinzu, indem Sie Java Diagram API verwenden.
---
## **Erstellen einer Diagram**
 Mit Aspose.Diagram for Java können Sie Microsoft Visio Diagramme aus Ihren eigenen Anwendungen lesen und erstellen, ohne Microsoft Office Automatisierung. Der erste Schritt beim Erstellen neuer Dokumente ist das Erstellen einer diagram. Dann[Fügen Sie Formen und Verbinder hinzu](https://docs.aspose.com/diagram/java/add-retrieve-copy-and-read-visio-shape-data/)um die diagram aufzubauen. Verwenden Sie den Standardkonstruktor von[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) Klasse, um eine neue diagram zu erstellen.
### **Programmierbeispiel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Wasserzeichen zu visio auf der Seite hinzufügen
1. Rufen Sie die Save-Methode des Klassenobjekts Diagram auf und übergeben Sie auch den vollständigen Dateipfad und das DiagramSaveOptions-Objekt.
### **Programmierbeispiel für Wasserzeichen hinzufügen**
Der folgende Beispielcode zeigt, wie man Wasserzeichen in Visio diagram hinzufügt.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWatermarkToVisio.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");

double pinx = page.getPageSheet().getPageProps().getPageWidth().getValue() / 2;
double piny = page.getPageSheet().getPageProps().getPageHeight().getValue() / 2;
double width = page.getPageSheet().getPageProps().getPageWidth().getValue();
double height =page.getPageSheet().getPageProps().getPageHeight().getValue();
    
//Add watermark
Shape shape = page.addText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);

// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
