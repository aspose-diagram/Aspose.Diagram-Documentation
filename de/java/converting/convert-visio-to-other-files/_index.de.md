---
title:  Konvertieren Sie Visio in andere Formate
linktitle:  Konvertieren Sie Visio in andere Formate
type: docs
weight: 40
url: /de/java/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Exportieren nach XML**
 In diesem Artikel wird erläutert, wie Sie eine Microsoft Visio diagram mithilfe von XML in XML exportieren[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- VDX definiert ein XML diagram.
- VTX definiert eine XML-Vorlage.
- VSX definiert eine XML-Schablone.

 Das[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) Die Konstruktoren der Klasse lesen eine diagram und die Save-Methode wird verwendet, um eine diagram in einem anderen Dateiformat zu speichern oder zu exportieren. Die Codeausschnitte in diesem Artikel zeigen, wie die Save-Methode zum Speichern einer Visio-Datei verwendet wird[VDX](/diagram/de/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/de/java/how-to-convert-a-visio-diagram/) und[VSX](/diagram/de/java/how-to-convert-a-visio-diagram/).

Das folgende Bild zeigt die diagram, die in den folgenden Codeausschnitten exportiert wird. Die exportierte Datei wird vor jedem Codeausschnitt angezeigt.

**A Microsoft Visio diagram kurz vor dem Export.**

![todo: Bild_alt_Text](http://i.imgur.com/XWajazh.png)
### **Exportieren von VSD zu VDX**
VDX ist ein schemabasiertes XML-Dateiformat, mit dem Sie Diagramme in einem Format speichern können, das andere Produkte als Microsoft Visio lesen können. Es ist ein nützliches Format zum Übertragen von Diagrammen zwischen Softwareanwendungen und zum Aufbewahren bearbeitbarer Daten.

So exportieren Sie eine VSD diagram in VDX:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VDX zu schreiben.

**Die exportierte VDX-Datei.**

![todo: Bild_alt_Text](http://i.imgur.com/OJ1jpgh.png)
### **Exportieren von VSD bis VSX**
VSX ist ein XML-Format zum Definieren von Schablonen, den Grundobjekten, aus denen ein diagram aufgebaut ist. Wenn eine Visio-Datei in VSX konvertiert wird, werden nur die Schablonen exportiert.

So exportieren Sie eine VSD diagram in VSX:

- Erstellen Sie eine Instanz der Klasse Diagram.
- Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VSX zu schreiben.

Das folgende Bild zeigt die Ausgabedatei VSX. Beachten Sie, dass die in diagram verwendeten Schablonen, nicht diagram selbst, exportiert werden.

**Die exportierte VSX-Datei.**

![todo: Bild_alt_Text](http://i.imgur.com/gkZrxCN.png)
### **Exportieren Sie VSD bis VTX**
TVX ist eine XML-Darstellung einer Vorlagendatei und speichert die Einstellungen für das Dokument.

So exportieren Sie eine VSD diagram in VTX:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Rufen Sie die Save-Methode der Klasse diagram auf, um die Zeichnungsdatei Visio im Format VTX zu schreiben.

Das folgende Bild zeigt die Ausgabedatei VTX.

**Die Ausgabedatei VTX.**

![todo: Bild_alt_Text](http://i.imgur.com/E6pUvGD.jpg)
### **Exportieren in ein XML-Programmierbeispiel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXML.class);

/* 1. Exporting VSDX to VDX */
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

//Save input VSD as VDX
diagram.save(dataDir + "ExportToXML_Out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
        
//Save input VSD as VSX
diagram.save(dataDir + "ExportToXML_Out.vsx", SaveFileFormat.VSX);
        
/* 3. Export VSD to VTX */
//Save input VSD as VTX
diagram.save(dataDir + "ExportToXML_Out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}

## **Exporting to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
 Verwenden Sie die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Das Quelldokument.**

![todo: Bild_alt_Text](http://i.imgur.com/P3gaA34.png)

To export VSD diagram to XPS:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.

Das folgende Bild zeigt die Ausgabedatei XPS.

**The output XPS.**

![todo: Bild_alt_Text](http://i.imgur.com/1ESRxSy.png)
### **Exporting to XPS Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXPS.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir+ "ExportToXPS.vsd");

// Save as XPS
diagram.save(dataDir + "ExportToXPS_Out.xps", SaveFileFormat.XPS);

{{< /highlight >}}

## **Exporting a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Verwenden Sie die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

To export VSD diagram to SVG, perform the following steps:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Exporting Diagram to SVG Programming Sample**
The code samples show how to export a diagram to SVG using Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToSVG.class);

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save as SVG
diagram.save(dataDir+ "ExportToSVG_Out.svg", SaveFileFormat.SVG);

{{< /highlight >}}

## **Exporting a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Verwenden Sie die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

So exportieren Sie eine VSD diagram in XAML:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the class' Save method and set XAML as the export format.
### **Exporting to XAML Programming Sample**
The code sample show how to export a diagram to XAML using Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXAML.class); 

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");

// save as XAML
diagram.save(dataDir + "ExportToXAML_Out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}


## **Konvertieren Visio Zeichnen mit ausgewählten Formen**
Mit Aspose.Diagram API können Entwickler eine Gruppe von Formen auswählen, um eine Visio-Zeichnung in ein beliebiges anderes unterstütztes Format zu konvertieren. Die RenderingSaveOptions-Klasse bietet ein Shapes-Member, um die Gruppe von Formen zu verwalten. Jede Speicheroptionsklasse ist die erweiterte Form der RenderingSaveOptions-Klasse.

So exportieren Sie eine Visio-Zeichnung mit ausgewählten Formen:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Erstellen Sie eine Instanz einer beliebigen SaveOption-Klasse, um die hier beschriebenen Einstellungen anzugeben:[Geben Sie Visio Speicheroptionen an](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. Rufen Sie die Methode save des Klassenobjekts Diagram auf und übergeben Sie das Klassenobjekt save option als Parameter.
### **Konvertieren Visio Programmierbeispiel für Zeichnen mit ausgewählten Formen**
Das Codebeispiel zeigt, wie eine Zeichnung mit ausgewählten Visio-Formen exportiert wird.


{{< highlight java >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";
		
// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.getPages().get(0).getShapes().getShape(1));
shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing
diagram.save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
