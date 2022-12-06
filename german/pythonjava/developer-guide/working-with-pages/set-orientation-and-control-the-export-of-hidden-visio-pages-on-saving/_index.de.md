---
title: Legen Sie die Ausrichtung fest und steuern Sie den Export versteckter Visio-Seiten beim Speichern
type: docs
weight: 20
url: /de/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Ändern Sie ein Visio-Seitenlayout in Hoch- oder Querformat**
Aspose.Diagram for Python via Java API allows developers to set the orientation of the Visio drawing page programmatically. This help topic explains how to accomplish this task.

Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the print properties. The `PrintPageOrientation` field of the print properties allows to rotate the page. It offers three options as Portrait, Landscape and same as on the printer. The PrintPageOrientation field can be set programmatically using Aspose.Diagram for Python via Java API.

Dieses Beispiel funktioniert wie folgt:

1. Laden Sie ein vorhandenes Visio diagram in das Klassenobjekt Diagram.
1. Extrahieren Sie eine Visio-Seite
1. Legen Sie die Ausrichtung als Hochformat, Querformat oder dieselbe wie auf dem Drucker fest.
1. Speichern Sie die Visio diagram.

### **Beispiel für die Programmierung der Orientierung einstellen**
Das folgende Codebeispiel zeigt, wie die Ausrichtung der Seite Visio festgelegt wird.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-SetVisioPageOrientation.py" >}}

## **Steuern Sie den Export versteckter Visio-Seiten beim Speichern**
Aspose.Diagram for Python via Java API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram for Python via Java API because its option is already available through the cell UIVisibility in the page ShapeSheet.

### **Blenden Sie eine Seite in der Visio Diagram aus und legen Sie die Exportoption fest**
Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the page properties. The `UIVisibility` field of the page properties allows to hide the page. Developers can then use `exportHiddenPage` property which is added in the `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` and `PdfSaveOptions` classes.

#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExporToHiddenVisioPagesToPdf.py" >}}

#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToHtml.py" >}}

#### **Legen Sie die Exportoption für das Bild fest**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein diagram im Bildformat gespeichert wird.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToImage.py" >}}

#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToSVG.py" >}}
