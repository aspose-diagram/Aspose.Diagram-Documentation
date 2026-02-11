---
title: Holen Sie sich Papierbreite und Seitenhöhe
type: docs
weight: 50
url: /de/net/get-paper-width-and-height-of-page/
description: In diesem Abschnitt wird erläutert, wie Sie die Papiergröße der Seite visio mit Aspose.Diagram erhalten.
---
## **Mögliche Nutzungsszenarien**

Manchmal müssen Sie die Breite und Höhe des Papierformats kennen, da es in der Seiteneinrichtung der Seite festgelegt wurde. Bitte verwenden Sie die[**PageProps.Seitenbreite**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)und[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)Eigenschaften für diesen Zweck.

## **Holen Sie sich die Seitenbreite und -höhe der Seitenstütze der Seite**

 Der folgende Beispielcode erläutert die Verwendung von[**PageProps.Seitenbreite**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)und[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)Eigenschaften.

### **Beispielcode**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");

// Get page's width and height
double pagewidth = page.PageSheet.PageProps.PageWidth.Value;
double pageheight = page.PageSheet.PageProps.PageHeight.Value;

{{< /highlight >}}
```
