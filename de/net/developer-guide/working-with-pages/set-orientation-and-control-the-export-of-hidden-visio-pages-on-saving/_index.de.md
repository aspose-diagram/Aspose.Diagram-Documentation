---
title: Legen Sie die Ausrichtung fest und steuern Sie den Export versteckter Visio-Seiten beim Speichern
type: docs
weight: 20
url: /de/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: In diesem Abschnitt wird erläutert, wie Sie das Seitenlayout mit Aspose.Diagram festlegen.
---
## **Ändern Sie ein Visio-Seitenlayout in Hoch- oder Querformat**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API ermöglicht es Entwicklern, die Ausrichtung der Zeichenseite Visio programmgesteuert festzulegen. In diesem Hilfethema wird erläutert, wie Sie diese Aufgabe ausführen.

 Aspose.Diagram for .NET API hat die[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse, die ein Zeichenblatt Visio darstellt. Die PageSheet-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, macht auch die Druckeigenschaften verfügbar. Das Feld PrintPageOrientation der Druckeigenschaften ermöglicht das Drehen der Seite. Es bietet drei Optionen wie Hochformat, Querformat und die gleichen wie auf dem Drucker. Das Feld PrintPageOrientation kann programmgesteuert mit Aspose.Diagram API festgelegt werden.

Dieses Beispiel funktioniert wie folgt:

1. Laden Sie ein vorhandenes Visio diagram in das Klassenobjekt Diagram.
1. Extrahieren Sie eine Visio-Seite
1. Legen Sie die Ausrichtung als Hochformat, Querformat oder dieselbe wie auf dem Drucker fest.
1. Speichern Sie die Visio diagram.
### **Beispiel für die Programmierung der Orientierung einstellen**
Das folgende Codebeispiel zeigt, wie die Ausrichtung der Seite Visio festgelegt wird.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Page orientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;
// Save Visio
diagram.Save(dataDir + "SetPageOrientation_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Steuern Sie den Export versteckter Visio-Seiten beim Speichern**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Blenden Sie eine Seite in der Visio Diagram aus und legen Sie die Exportoption fest**
 Aspose.Diagram for .NET API hat die[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse, die ein Zeichenblatt Visio darstellt. Die PageSheet-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, macht auch die Seiteneigenschaften verfügbar. Das Feld UIVisibility der Seiteneigenschaften ermöglicht das Ausblenden der Seite. Entwickler können dann die ExportHiddenPage-Eigenschaft verwenden, die in den Klassen SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions und PdfSaveOptions hinzugefügt wird.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToPDF_out.pdf", options);

{{< /highlight >}}

#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToHTML_out.html", options);

{{< /highlight >}}

#### **Legen Sie die Exportoption für das Bild fest**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein diagram im Bildformat gespeichert wird.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToImage_out.jpeg", options);

{{< /highlight >}}

#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export guide shapes 
options.ExportGuideShapes = false;
// Set save format
options.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;
// Set SVG fit to view port
options.SVGFitToViewPort = true;
// Set export element as Rectangle
options.ExportElementAsRectTag = true;


// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToSVG_out.svg", options);

{{< /highlight >}}

#### **Set the Export Option for XPS**
The code below shows how to set save options before saving a diagram to XPS format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
XPSSaveOptions options = new XPSSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToXPS_out.xps", options);

{{< /highlight >}}

