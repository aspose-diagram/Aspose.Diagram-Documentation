---
title:  Konvertieren Sie Visio in andere Formate
linktitle:  Konvertieren Sie Visio in andere Formate
type: docs
weight: 40
url: /de/net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Nach XML exportieren**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}


 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram mithilfe von XML in XML exportieren[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX definiert ein XML diagram.
- VTX definiert eine XML-Vorlage.
- VSX definiert eine XML-Schablone.

 Das[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Die Konstruktoren der Klasse lesen eine diagram und die Save-Methode wird verwendet, um eine diagram in einem anderen Dateiformat zu speichern oder zu exportieren. Die Codeausschnitte in diesem Artikel zeigen, wie die Save-Methode zum Speichern einer Visio-Datei verwendet wird[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/) und[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
            
/* 1. Exporting VSDX to VDX */
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

// Save input VSD as VDX
diagram.Save(dataDir + "ExportToXML_out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
            
// Save input VSD as VSX
diagram.Save(dataDir + "ExportToXML_out.vsx", SaveFileFormat.VSX);
            
/* 3. Export VSD to VTX */
// Save input VSD as VTX
diagram.Save(dataDir + "ExportToXML_out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}


## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.
 Verwenden Sie die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Das Quelldokument.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Open a VSD file
Diagram diagram = new Diagram(dataDir + "LayOutShapesInCompactTreeStyle.vdx");

// Save diagram to an XPS format
diagram.Save(dataDir + "ExportToXPS_out.xps", SaveFileFormat.XPS);

{{< /highlight >}}


## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Verwenden Sie die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

To export VSD diagram to SVG, perform the following steps:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save SVG Output file
diagram.Save(dataDir + "Output.svg", SaveFileFormat.SVG);

{{< /highlight >}}

## **Export to SWF**
This article explains how to export a Microsoft Visio diagram to SWF using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Verwenden Sie die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors to read the diagram files and then the Diagram class' Save method to export the diagram to SWF format. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**Geben Sie diagram ein.**|
|:- |
|![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_7.png)|

Nach dem Code gibt es ein Bild der Ausgabe.

To export VSD diagram to SWF::

- Erstellen Sie eine Instanz der Klasse Diagram.
- Call the Diagram class' Save method and provide SWF format to export your diagram to SWF.
### **Embedded Viewer-Programmierbeispiel**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}

### **Ohne Viewer Programmierbeispiel**
The SWF file created by these code snippets include an SWF viewer. Exclude the SWF viewer from the file using the following code.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Instantiate Diagram Object and open VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSWFWithoutViewer.vsd");

// Instantiate the Save Options
SWFSaveOptions options = new SWFSaveOptions();

// Set Save format as SWF
options.SaveFormat = SaveFileFormat.SWF;

// Exclude the embedded viewer
options.ViewerIncluded = false;

// Save the resultant SWF file
diagram.Save(dataDir + "ExportToSWFWithoutViewer_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}

## **Export a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Verwenden Sie die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

So exportieren Sie eine VSD diagram in XAML:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the class' Save method and set XAML as the export format.
### **Export Microsoft Visio Drawing to XAML**
The code sample show how to export a diagram to XAML using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");
// Save diagram
diagram.Save(dataDir + "ExportToXAML_out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}

## **Konvertieren Visio Zeichnen mit ausgewählten Formen**
Mit Aspose.Diagram API können Entwickler eine Gruppe von Formen auswählen, um eine Visio-Zeichnung in ein beliebiges anderes unterstütztes Format zu konvertieren. Die RenderingSaveOptions-Klasse bietet ein Shapes-Member, um die Gruppe von Formen zu verwalten. Jede Speicheroptionsklasse ist die erweiterte Form der RenderingSaveOptions-Klasse.

So exportieren Sie eine Visio-Zeichnung mit ausgewählten Formen:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz einer beliebigen SaveOption-Klasse, um die hier beschriebenen Einstellungen anzugeben:[Geben Sie Visio Speicheroptionen an](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. Rufen Sie die Methode Save des Klassenobjekts Diagram auf und übergeben Sie das Klassenobjekt save option als Parameter.
### **Konvertieren Visio Programmierbeispiel für Zeichnen mit ausgewählten Formen**
Das Codebeispiel zeigt, wie eine Zeichnung mit ausgewählten Visio-Formen exportiert wird.


{{< highlight csharp >}}
// the path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.Add(diagram.Pages[0].Shapes.GetShape(1));
shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing
diagram.Save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
