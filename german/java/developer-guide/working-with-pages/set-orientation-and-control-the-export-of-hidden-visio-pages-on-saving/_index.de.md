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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-SetVisioPageOrientation-SetVisioPageOrientation.java" >}}
## **Steuern Sie den Export versteckter Visio-Seiten beim Speichern**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Blenden Sie eine Seite in der Visio Diagram aus und legen Sie die Exportoption fest**
 Aspose.Diagram for Java API hat die[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Klasse, die ein Zeichenblatt Visio darstellt. Die PageSheet-Eigenschaft, die von der Page-Klasse verfügbar gemacht wird, macht auch die Seiteneigenschaften verfügbar. Das Feld UIVisibility der Seiteneigenschaften ermöglicht das Ausblenden der Seite. Entwickler können dann die ExportHiddenPage-Eigenschaft verwenden, die in den Klassen SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions und PdfSaveOptions hinzugefügt wird.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExporToHiddenVisioPagesToPdf-ExporToHiddenVisioPagesToPdf.java" >}}
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToHtml-ExportOfHiddenVisioPagesToHtml.java" >}}
#### **Legen Sie die Exportoption für das Bild fest**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein diagram im Bildformat gespeichert wird.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.java" >}}
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.java" >}}
