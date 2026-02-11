---
title: Aktivieren Sie Seite automatisch erweitern
type: docs
weight: 10
url: /de/java/check-page-autoexpand/
description: In diesem Abschnitt wird erläutert, wie Sie überprüfen oder ändern, ob die Seite in einer visio-Datei mit Aspose.Diagram automatisch erweitert wird.
---
## **Überprüfen Sie die Seite AutoExpand**

 Das[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Die Pages-Eigenschaft, die von der[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten.
 Das[PageRequisiten](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) -Objekt stellt die Seitenattribute dar, z. B. Seitenbreite, -höhe und -skalierung. Diese Eigenschaft kann verwendet werden, um die automatische Erweiterung der Seite zu überprüfen.

Verwenden Sie die PageProps-Eigenschaft, um die automatische Erweiterung der Seite zu überprüfen.
### **Überprüfen Sie das Beispiel für die Programmierung der Seite AutoExpand**
Der folgende Codeabschnitt überprüft die automatische Erweiterung der Seite von einem diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

