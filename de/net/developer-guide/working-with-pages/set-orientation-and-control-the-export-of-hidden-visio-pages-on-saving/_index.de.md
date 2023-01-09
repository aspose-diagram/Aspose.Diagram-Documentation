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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Steuern Sie den Export versteckter Visio-Seiten beim Speichern**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Blenden Sie eine Seite in der Visio Diagram aus und legen Sie die Exportoption fest**
 Aspose.Diagram for .NET API hat die[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse, die ein Zeichenblatt Visio darstellt. Die PageSheet-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, macht auch die Seiteneigenschaften verfügbar. Das Feld UIVisibility der Seiteneigenschaften ermöglicht das Ausblenden der Seite. Entwickler können dann die ExportHiddenPage-Eigenschaft verwenden, die in den Klassen SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions und PdfSaveOptions hinzugefügt wird.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Legen Sie die Exportoption für das Bild fest**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein diagram im Bildformat gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **Set the Export Option for XPS**
The code below shows how to set save options before saving a diagram to XPS format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
