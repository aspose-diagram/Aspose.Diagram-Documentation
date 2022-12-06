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
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF**
### **Diagram Programmierbeispiel speichern**
Das folgende Beispiel speichert ein Dokument in einer Datei.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Festlegen von Visio Speicheroptionen**
 Es gibt einige[Diagram.Save]() Methodenüberladungen, die ein SaveOptions-Objekt akzeptieren. Dies sollte ein Objekt einer Klasse sein, die von der Klasse SaveOptions abgeleitet ist. Jedes Speicherformat hat eine entsprechende Klasse, die Speicheroptionen für dieses Speicherformat enthält. Beispielsweise gibt es PdfSaveOptions für das Speicherformat SaveFileFormat.PDF.
### **Visio Diagram Speicheroptionen**
Diese Beispiele zeigen, wie Sie:

- [Verwenden Sie Diagram Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie die PDF-Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie HTML-Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie Bildspeicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie die SVG-Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Verwenden Sie die SWF-Speicheroptionen](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Verwendung der Diagram-Speicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format Visio gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **Verwendung der PDF-Speicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im PDF-Format gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **Verwendung der HTML-Speicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im HTML-Dateiformat gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **Verwendung der Bildspeicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Bilddateiformat gespeichert wird.



{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


Verwendung der SVG-Speicheroptionen

Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im SVG-Format gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


Verwendung der SWF-Speicheroptionen

Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im SWF-Format gespeichert wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

Manchmal müssen Entwickler Visio-Diagramme programmgesteuert speichern oder in verschiedene Dateiformate exportieren (wie VDX, PDF, JPEG usw.).
## **VSD-Datei in verschiedenen Dateiformaten speichern (VDX, PDF und JPEG)**
 Dieser Artikel enthält ein Codebeispiel, das die Verwendung veranschaulicht[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) und[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) um eine Microsoft Visio VSD-Datei programmgesteuert in einer VDX-Datei, PDF-Datei oder JPEG-Datei zu speichern. Unten finden Sie parallele Codeausschnitte für VSTO und Aspose.Diagram for .NET, die erklären, wie eine VSD-Datei in verschiedenen Dateiformaten gespeichert wird. Sie werden feststellen, dass der Code Aspose.Diagram kürzer ist. Fühlen Sie sich frei, den Code zu verwenden und ihn an Ihre spezifischen Bedürfnisse anzupassen.
### **Speichern einer VSD-Datei in anderen Formaten mit VSTO**
Mit VSTO können Sie mit Microsoft Visio-Dateien programmieren. So speichern Sie eine Datei in anderen Formaten:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Laden Sie die diagram.
1. Speichern unter VDX, PDF und JPEG.
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
1. Speichern Sie die diagram bis VSX, PDF und JPEG.
#### **Speichern der VSD-Datei mit Aspose.Diagram for .NET Programmierbeispiel**
{{% alert color="primary" %}} 

mit Aspose.Diagram;
Importiert Aspose.Diagram

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
