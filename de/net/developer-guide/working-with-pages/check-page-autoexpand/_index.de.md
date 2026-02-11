---
title: Aktivieren Sie Seite automatisch erweitern
type: docs
weight: 10
url: /de/net/check-page-autoexpand/
description: In diesem Abschnitt wird erläutert, wie Sie überprüfen oder ändern, ob die Seite in einer visio-Datei mit Aspose.Diagram automatisch erweitert wird.
---
## **Seitengröße ändern**

 Das[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page)Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Die Pages-Eigenschaft, die von der[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten.
 Das[PageRequisiten](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) -Objekt stellt die Seitenattribute dar, z. B. Seitenbreite, -höhe und -skalierung. Diese Eigenschaft kann verwendet werden, um die automatische Erweiterung der Seite zu überprüfen.

Verwenden Sie die PageProps-Eigenschaft, um die automatische Erweiterung der Seite zu überprüfen.
### **Programmierbeispiel für die Einstellung der Seitengröße**
Der folgende Codeabschnitt überprüft die automatische Erweiterung der Seite von einem diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
