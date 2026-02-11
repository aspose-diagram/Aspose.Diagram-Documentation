---
title:  Konvertieren Sie Visio in andere Formate
linktitle:  Konvertieren Sie Visio in andere Formate
type: docs
weight: 40
url: /de/python-net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Nach XML exportieren**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}


 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram mithilfe von XML in XML exportieren[Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

- VDX definiert ein XML diagram.
- VTX definiert eine XML-Vorlage.
- VSX definiert eine XML-Schablone.

 Die Konstruktoren der Klasse [Diagram] lesen einen diagram und die Save-Methode wird verwendet, um einen diagram in einem anderen Dateiformat zu speichern oder zu exportieren. Die Codeausschnitte in diesem Artikel zeigen, wie die Save-Methode zum Speichern einer Visio-Datei verwendet wird[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/) und[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

Das folgende Bild zeigt die diagram, die in den folgenden Codeausschnitten exportiert wird. Die exportierte Datei wird vor jedem Codeausschnitt angezeigt.

|**A Microsoft Visio diagram kurz vor dem Export.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_3.png)|

### **Exportieren Sie VSD bis VDX**
VDX ist ein schemabasiertes XML-Dateiformat, mit dem Sie Diagramme in einem Format speichern können, das andere Produkte als Microsoft Visio lesen können. Es ist ein nützliches Format zum Übertragen von Diagrammen zwischen Softwareanwendungen und zum Aufbewahren bearbeitbarer Daten.

So exportieren Sie eine VSD diagram in VDX:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VDX zu schreiben.

|**Die exportierte VDX-Datei.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_4.png)|

### **Export von VSD bis VSX**
VSX ist ein XML-Format zum Definieren von Schablonen, den Grundobjekten, aus denen ein diagram aufgebaut ist. Wenn eine Visio-Datei in VSX konvertiert wird, werden nur die Schablonen exportiert.

So exportieren Sie eine VSD diagram in VSX:

- Erstellen Sie eine Instanz der Klasse Diagram.
- Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VSX zu schreiben.
### **Exportieren Sie VSD bis VTX**
TVX ist eine XML-Darstellung einer Vorlagendatei und speichert die Einstellungen für das Dokument.

So exportieren Sie eine VSD diagram in VTX:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse diagram auf, um die Zeichnungsdatei Visio im Format VTX zu schreiben.
### **Microsoft Visio Zeichnung in XML exportieren**
Die Codebeispiele zeigen, wie Microsoft Visio Drawing in XML mit C# exportiert wird.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the vdx format
diagram.save("Visio_out.vdx", SaveFileFormat.VDX)

#// Save diagram in the vtx format
diagram.save("Visio_out.vtx", SaveFileFormat.VTX)

#// Save diagram in the vsx format
diagram.save("Visio_out.vsx", SaveFileFormat.VSX)
{{< /highlight >}}


## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.
Verwenden Sie den Klassenkonstruktor [Diagram], um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Das Quelldokument.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the xps format
diagram.save("Visio_out.xps", SaveFileFormat.XPS)
{{< /highlight >}}


## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Verwenden Sie den Klassenkonstruktor [Diagram], um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

To export VSD diagram to SVG, perform the following steps:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the svg format
diagram.save("Visio_out.svg", SaveFileFormat.SVG)
{{< /highlight >}}


So exportieren Sie eine Visio-Zeichnung mit ausgewählten Formen:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz einer beliebigen SaveOption-Klasse, um die hier beschriebenen Einstellungen anzugeben:[Geben Sie Visio Speicheroptionen an](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Rufen Sie die Methode Save des Klassenobjekts Diagram auf und übergeben Sie das Klassenobjekt save option als Parameter.
### **Konvertieren Visio Programmierbeispiel für Zeichnen mit ausgewählten Formen**
Das Codebeispiel zeigt, wie eine Zeichnung mit ausgewählten Visio-Formen exportiert wird.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.SVGSaveOptions()
shapes = options.shapes;
#// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.pages[0].shapes.get_shape(1));
shapes.add(diagram.pages[0].shapes.get_shape(2));
    
#// Save one page only, by page index
options.page_index = 0
    
#// Save resultant svg file
diagram.save("ExportToSvg_out.svg", options)
{{< /highlight >}}
