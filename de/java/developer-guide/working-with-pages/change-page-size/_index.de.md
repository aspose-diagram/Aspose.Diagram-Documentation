---
title: Seitengröße ändern
type: docs
weight: 10
url: /de/java/change-page-size/
description: In diesem Abschnitt wird erläutert, wie Sie die Seitengröße in einer visio-Datei mit Aspose.Diagram ändern.
---
## **Seitengröße ändern**

 Das[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Die Pages-Eigenschaft, die von der[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten.
 Das[PageRequisiten](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) -Objekt stellt die Seitenattribute dar, z. B. Seitenbreite, -höhe und -skalierung. Diese Eigenschaft kann verwendet werden, um die Seitengröße zu ändern.

Verwenden Sie die PageProps-Eigenschaft, um die Seitengröße zu ändern.
### **Programmierbeispiel für die Einstellung der Seitengröße**
Der folgende Codeabschnitt ändert die Seitengröße von diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
