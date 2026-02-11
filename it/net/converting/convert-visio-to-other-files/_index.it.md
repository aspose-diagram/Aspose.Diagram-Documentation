---
title:  Converti Visio in altri formati
linktitle:  Converti Visio in altri formati
type: docs
weight: 40
url: /it/net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Esporta in XML**
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


 Questo articolo spiega come esportare un Microsoft Visio diagram in XML utilizzando[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX definisce un XML diagram.
- VTX definisce un modello XML.
- VSX definisce uno stencil XML.

 Il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' leggono un diagram e il metodo Save viene utilizzato per salvare o esportare un diagram in un formato di file diverso. I frammenti di codice in questo articolo mostrano come utilizzare il metodo Save per salvare un file Visio in[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/) e[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

L'immagine seguente mostra lo diagram che viene esportato nei frammenti di codice seguenti. Il file esportato viene mostrato prima di ogni frammento di codice.

|**A Microsoft Visio diagram in procinto di essere esportato.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_3.png)|

### **Esporta da VSD a VDX**
VDX è un formato di file XML basato su schema che consente di salvare i diagrammi in un formato leggibile da prodotti diversi da Microsoft Visio. È un formato utile per trasferire diagrammi tra applicazioni software e conservare dati modificabili.

Per esportare un VSD da diagram a VDX:

1. Creare un'istanza della classe Diagram.
1. Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VDX.

|**Il file VDX esportato.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_4.png)|

### **Esporta da VSD a VSX**
VSX è un formato XML per definire gli stencil, gli oggetti di base da cui viene creato un diagram. Quando un file Visio viene convertito in VSX, vengono esportati solo gli stencil.

Per esportare un VSD da diagram a VSX:

- Creare un'istanza della classe Diagram.
- Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VSX.
### **Esporta da VSD a VTX**
TVX è una rappresentazione XML di un file modello e memorizza le impostazioni per il documento.

Per esportare un VSD da diagram a VTX:

1. Creare un'istanza della classe Diagram.
1. Chiamare il metodo Save della classe diagram per scrivere il file di disegno Visio nel formato VTX.
### **Esporta Microsoft Visio Disegno in XML**
Gli esempi di codice mostrano come esportare il disegno Microsoft Visio in XML utilizzando C#.


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
 Utilizzare il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Il documento di origine.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. Creare un'istanza della classe Diagram.
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

 Utilizzare il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

To export VSD diagram to SVG, perform the following steps:

1. Creare un'istanza della classe Diagram.
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

 Utilizzare il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors to read the diagram files and then the Diagram class' Save method to export the diagram to SWF format. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**Inserisci diagram.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_7.png)|

Dopo il codice, c'è un'immagine dell'output.

To export VSD diagram to SWF::

- Creare un'istanza della classe Diagram.
- Call the Diagram class' Save method and provide SWF format to export your diagram to SWF.
### **Esempio di programmazione del visualizzatore incorporato**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}

### **Esempio di programmazione senza visualizzatore**
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

 Utilizzare il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

Per esportare un VSD da diagram a XAML:

1. Creare un'istanza della classe Diagram.
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

## **Converti Visio Disegno con forme selettive**
Utilizzando Aspose.Diagram API, gli sviluppatori possono selezionare un gruppo di forme per convertire un disegno Visio in qualsiasi altro formato supportato. La classe RenderingSaveOptions offre un membro Shapes per mantenere il gruppo di forme. Ogni classe di opzione di salvataggio è la forma estesa della classe RenderingSaveOptions.

Per esportare un disegno Visio con forme selettive:

1. Creare un'istanza della classe Diagram.
1. Crea un'istanza di qualsiasi classe SaveOption per specificare le impostazioni come descritto qui:[Specificare Visio Opzioni di salvataggio](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. Chiamare il metodo Save dell'oggetto di classe Diagram e passare l'oggetto di classe dell'opzione di salvataggio come parametro.
### **Conversione Visio Disegno con esempio di programmazione di forme selettive**
L'esempio di codice mostra come esportare un disegno con forme Visio selettive.


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
