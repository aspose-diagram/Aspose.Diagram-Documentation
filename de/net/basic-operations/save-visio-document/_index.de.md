---
title: Speichern Sie das Dokument Visio programmgesteuert
linktitle: Dokument Visio speichern
type: docs
weight: 30
url: /de/net/save-visio-document/
description: Auf dieser Seite wird beschrieben, wie Sie das Visio-Dokument in einer Datei speichern und mit der Aspose.Diagram-Bibliothek streamen.
---
## **Visio Übersicht zum Speichern von Zeichnungen**
 Verwenden Sie die[Diagram.Save]() Methode zum Speichern einer Microsoft Visio Zeichnung. Es gibt Überladungen, die das Speichern einer Zeichnung in einer Datei ermöglichen. Die Zeichnung kann in jedem von Aspose.Diagram unterstützten Speicherformat gespeichert werden. Eine Liste aller unterstützten Speicherformate finden Sie unter[SaveFileFormat]() Aufzählung.
## **Speichern Visio Diagram**
 Die Diagram-Klasse des Aspose.Diagram API stellt eine Visio-Zeichnung dar, und Entwickler können ihr Visio diagram-Objekt in jedem unterstützten Dateiformat speichern. Um eine Microsoft Visio-Datei zu speichern, verwenden Sie einfach die[Diagram.Save]()-Methode akzeptiert sie einen Dateinamen mit vollständigem Pfad oder ein Dateistromobjekt. Aspose.Diagram API leitet das Speicherformat aus der Dateierweiterung ab und bietet außerdem einen zusätzlichen SaveFileFormat-Parameter zur Angabe des Ausgabedateiformats.
### **Speichern Sie eine Visio Diagram in einem beliebigen unterstützten Dateiformat**
Mit Aspose.Diagram API können Entwickler Visio diagram in jedem unterstützten Dateiformat speichern, wie unten aufgeführt:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Diagram Programmierbeispiel speichern**
Das folgende Beispiel speichert ein Dokument in einer Datei.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Festlegen von Visio Speicheroptionen**
 Es gibt einige[Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Speicheroptionen**
Diese Beispiele zeigen, wie Sie:

- [Verwenden Sie Diagram Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie PDF Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie HTML Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie Bildspeicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie SVG Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie SWF Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Verwendung der Diagram-Speicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format Visio gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **Verwendung der PDF-Speicheroptionen**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **Verwendung der HTML-Speicheroptionen**
The code below shows how to set save options before saving a document to HTML file format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **Verwendung der Bildspeicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Bilddateiformat gespeichert wird.



{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


Verwendung der SVG-Speicheroptionen

Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format SVG gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


Verwendung der SWF-Speicheroptionen

Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format SWF gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).
## **Save VSD file to different file formats (VDX, PDF and JPEG)**
 Dieser Artikel enthält ein Codebeispiel, das die Verwendung veranschaulicht[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) und[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) to save a Microsoft Visio VSD file to a VDX file, PDF file or a JPEG file programmatically. Below are parallel code snippets for VSTO and Aspose.Diagram for .NET that explains how to save a VSD file into different file formats. You'll notice that the Aspose.Diagram code is shorter. Feel free to use the code and change it to meet your specific needs.
### **Speichern einer VSD-Datei in anderen Formaten mit VSTO**
Mit VSTO können Sie mit Microsoft Visio-Dateien programmieren. So speichern Sie eine Datei in anderen Formaten:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Laden Sie die diagram.
1. Save to VDX, PDF and JPEG.
1. Beenden Sie das Anwendungsobjekt Visio.
#### **Speichern einer VSD-Datei mit VSTO-Programmierbeispiel**
{{% alert color="primary" %}} 

mit Visio = Microsoft.Office.Interop.Visio;
Importe Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withVSTO-SaveDiagramTo_VDX_PDF_JPEG_withVSTO.cs" >}}
### ` `**Speichern von VSD-Dateien in anderen Formaten mit Aspose.Diagram for .NET**
Mit Aspose.Diagram brauchen Entwickler Microsoft Office Visio nicht in der Maschine und können unabhängig von Microsoft Office Automation arbeiten.

Die folgenden Code-Snippets zeigen, wie Sie:

1. Laden Sie eine diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Speichern der VSD-Datei mit Aspose.Diagram for .NET Programmierbeispiel**
{{% alert color="primary" %}} 

mit Aspose.Diagram;
Importiert Aspose.Diagram

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
