---
title: Speichern Sie das Dokument Visio programmgesteuert
linktitle: Dokument Visio speichern
type: docs
weight: 30
url: /de/java/save-visio-document/
description: Auf dieser Seite wird beschrieben, wie Sie das Visio-Dokument in einer Datei speichern und mit der Aspose.Diagram-Bibliothek streamen.
---
## **Visio Übersicht zum Speichern von Zeichnungen**
 Verwenden Sie die[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) Methode zum Speichern einer Microsoft Visio Zeichnung. Es gibt Überladungen, die das Speichern einer Zeichnung in einer Datei ermöglichen. Die Zeichnung kann in jedem von Aspose.Diagram unterstützten Speicherformat gespeichert werden. Eine Liste aller unterstützten Speicherformate finden Sie unter[SaveFileFormat](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat) Aufzählung.
## **Speichern Visio Diagram**
 Die Diagram-Klasse des Aspose.Diagram API stellt eine Visio-Zeichnung dar, und Entwickler können ihr Visio diagram-Objekt in jedem unterstützten Dateiformat speichern. Um eine Microsoft Visio-Datei zu speichern, verwenden Sie einfach die[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\))-Methode akzeptiert sie einen Dateinamen mit vollständigem Pfad oder ein Dateistromobjekt. Aspose.Diagram API leitet das Speicherformat von der Dateierweiterung ab und bietet außerdem einen zusätzlichen SaveFileFormat-Parameter, um das Ausgabedateiformat anzugeben.
### **Speichern Sie eine Visio Diagram in einem beliebigen unterstützten Dateiformat**
Mit Aspose.Diagram API können Entwickler Visio diagram in jedem unterstützten Dateiformat speichern, wie unten aufgeführt:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Diagram Programmierbeispiel speichern**
Das folgende Beispiel speichert ein Dokument in einer Datei.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Festlegen von Visio Speicheroptionen**
 Es gibt einige[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Speicheroptionen**
Diese Beispiele zeigen, wie Sie:

- [Verwenden Sie Diagram Speicheroptionen](/diagram/de/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Verwenden Sie PDF Speicheroptionen](/diagram/de/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Verwenden Sie HTML Speicheroptionen](/diagram/de/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Verwenden Sie Bildspeicheroptionen](/diagram/de/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Verwenden Sie SVG Speicheroptionen](/diagram/de/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Verwendung der Diagram-Speicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format Visio gespeichert wird.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Verwendung der PDF-Speicheroptionen**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Verwendung der HTML-Speicheroptionen**
The code below shows how to set save options before saving a document to a HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Verwendung der Bildspeicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument in einem Bildformat gespeichert wird.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Verwendung der SVG-Speicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format SVG gespeichert wird.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
