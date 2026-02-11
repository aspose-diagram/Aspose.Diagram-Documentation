---
title: Legen Sie die Ausrichtung fest und steuern Sie den Export versteckter Visio-Seiten beim Speichern
type: docs
weight: 20
url: /de/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Ändern Sie ein Visio-Seitenlayout in Hoch- oder Querformat**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API ermöglicht es Entwicklern, die Ausrichtung der Zeichenseite Visio programmgesteuert festzulegen. In diesem Hilfethema wird erläutert, wie Sie diese Aufgabe ausführen.

 Aspose.Diagram for Java API hat die[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Klasse, die ein Zeichenblatt Visio darstellt. Die PageSheet-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, macht auch die Druckeigenschaften verfügbar. Das Feld PrintPageOrientation der Druckeigenschaften ermöglicht das Drehen der Seite. Es bietet drei Optionen wie Hochformat, Querformat und die gleichen wie auf dem Drucker. Das Feld PrintPageOrientation kann programmgesteuert mit Aspose.Diagram API festgelegt werden.

Dieses Beispiel funktioniert wie folgt:

1. Laden Sie ein vorhandenes Visio diagram in das Klassenobjekt Diagram.
1. Extrahieren Sie eine Visio-Seite
1. Legen Sie die Ausrichtung als Hochformat, Querformat oder dieselbe wie auf dem Drucker fest.
1. Speichern Sie die Visio diagram.
### **Beispiel für die Programmierung der Orientierung einstellen**
Das folgende Codebeispiel zeigt, wie die Ausrichtung der Seite Visio festgelegt wird.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetVisioPageOrientation.class);  
// initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE);
// save Visio
diagram.save(dataDir + "SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Steuern Sie den Export versteckter Visio-Seiten beim Speichern**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Blenden Sie eine Seite in der Visio Diagram aus und legen Sie die Exportoption fest**
 Aspose.Diagram for Java API hat die[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Klasse, die ein Zeichenblatt Visio darstellt. Die PageSheet-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, macht auch die Seiteneigenschaften verfügbar. Das Feld UIVisibility der Seiteneigenschaften ermöglicht das Ausblenden der Seite. Entwickler können dann die ExportHiddenPage-Eigenschaft verwenden, die in den Klassen SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions und PdfSaveOptions hinzugefügt wird.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExporToHiddenVisioPagesToPdf.class);  
        
// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);

//Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToPDF_Out.pdf", options);

{{< /highlight >}}
```
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToHtml.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);
// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToHTML_Out.html", options);

{{< /highlight >}}
```
#### **Legen Sie die Exportoption für das Bild fest**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein diagram im Bildformat gespeichert wird.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToImage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);
// initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);

// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToImage_Out.jpeg", options);

{{< /highlight >}}
```
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToSVG.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// Set SVG fit to view port
options.setSVGFitToViewPort(true);
// Set export element as Rectangle
options.setExportElementAsRectTag(true);

// save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToSVG_Out.svg", options);

{{< /highlight >}}
```
