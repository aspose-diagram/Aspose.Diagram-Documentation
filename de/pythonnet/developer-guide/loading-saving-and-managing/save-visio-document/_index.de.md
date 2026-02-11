---
title: Speichern Sie das Dokument Visio programmgesteuert
linktitle: Dokument Visio speichern
type: docs
weight: 30
url: /de/python-net/save-visio-document/
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

- [Verwenden Sie Diagram Speicheroptionen](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Verwenden Sie PDF Speicheroptionen](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Verwenden Sie HTML Speicheroptionen](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Verwenden Sie Bildspeicheroptionen](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Verwenden Sie SVG Speicheroptionen](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Verwenden Sie SWF Speicheroptionen](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Verwendung der Diagram-Speicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format Visio gespeichert wird.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.DiagramSaveOptions(SaveFileFormat.VSDX)

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", options)
{{< /highlight >}}




#### **Verwendung der PDF-Speicheroptionen**
The code below shows how to set save options before saving a document to a PDF format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.PdfSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the pdf format
diagram.save("CreateNewVisio_out.pdf", options)
{{< /highlight >}}




#### **Verwendung der HTML-Speicheroptionen**
The code below shows how to set save options before saving a document to HTML file format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.HTMLSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the html format
diagram.save("Visio_out.html", options)
{{< /highlight >}}




#### **Verwendung der Bildspeicheroptionen**
Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Bilddateiformat gespeichert wird.




{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}



Verwendung der SVG-Speicheroptionen

Der folgende Code zeigt, wie Speicheroptionen festgelegt werden, bevor ein Dokument im Format SVG gespeichert wird.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as svg
options = saving.SVGSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the svg format
diagram.save("ExportPageToSvg_out.svg", options)
{{< /highlight >}}


Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).

### ` `**Saving VSD File to Other Formats with Aspose.Diagram for Python via .NET**
Mit Aspose.Diagram brauchen Entwickler Microsoft Office Visio nicht in der Maschine und können unabhängig von Microsoft Office Automation arbeiten.

Die folgenden Code-Snippets zeigen, wie Sie:

1. Laden Sie eine diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Saving VSD File with Aspose.Diagram for Python via .NET Programming Sample**
{{% alert color="primary" %}} 

Import aspose.diagram
von aspose.diagram importieren *

{{% /alert %}} 

**Beispiel:**


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save the diagram as VDX
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToVDXwithAspose_out.vdx"), SaveFileFormat.VDX)

#// Save as PDF
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToPDFwithAspose_out.pdf"), SaveFileFormat.PDF)

#// Save as JPEG
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToJPGwithAspose_out.jpg"), SaveFileFormat.JPEG)
{{< /highlight >}}

