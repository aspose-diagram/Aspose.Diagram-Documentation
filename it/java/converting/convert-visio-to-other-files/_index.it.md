---
title:  Converti Visio in altri formati
linktitle:  Converti Visio in altri formati
type: docs
weight: 40
url: /it/java/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Esportazione in XML**
 Questo articolo spiega come esportare un Microsoft Visio diagram in XML utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- VDX definisce un XML diagram.
- VTX definisce un modello XML.
- VSX definisce uno stencil XML.

 Il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' leggono un diagram e il metodo Save viene utilizzato per salvare o esportare un diagram in un formato di file diverso. I frammenti di codice in questo articolo mostrano come utilizzare il metodo Save per salvare un file Visio in[VDX](/diagram/it/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/it/java/how-to-convert-a-visio-diagram/) e[VSX](/diagram/it/java/how-to-convert-a-visio-diagram/).

L'immagine seguente mostra lo diagram che viene esportato nei frammenti di codice seguenti. Il file esportato viene mostrato prima di ogni frammento di codice.

**A Microsoft Visio diagram in procinto di essere esportato.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/XWajazh.png)
### **Esportazione da VSD a VDX**
VDX è un formato di file XML basato su schema che consente di salvare i diagrammi in un formato leggibile da prodotti diversi da Microsoft Visio. È un formato utile per trasferire diagrammi tra applicazioni software e conservare dati modificabili.

Per esportare un VSD da diagram a VDX:

1. Creare un'istanza della classe Diagram.
1. Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VDX.

**Il file VDX esportato.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/OJ1jpgh.png)
### **Esportazione da VSD a VSX**
VSX è un formato XML per definire gli stencil, gli oggetti di base da cui viene creato un diagram. Quando un file Visio viene convertito in VSX, vengono esportati solo gli stencil.

Per esportare un VSD da diagram a VSX:

- Creare un'istanza della classe Diagram.
- Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VSX.

L'immagine seguente mostra il file di output VSX. Si noti che vengono esportati gli stencil utilizzati in diagram, non lo stesso diagram.

**Il file VSX esportato.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/gkZrxCN.png)
### **Esporta da VSD a VTX**
TVX è una rappresentazione XML di un file modello e memorizza le impostazioni per il documento.

Per esportare un VSD da diagram a VTX:

1. Creare un'istanza della classe Diagram.
1. Chiamare il metodo Save della classe diagram per scrivere il file di disegno Visio nel formato VTX.

L'immagine seguente mostra il file di output VTX.

**Il file di output VTX.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/E6pUvGD.jpg)
### **Esempio di programmazione dell'esportazione in XML**
```
{{< highlight "java" >}}
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
```
## **Exporting to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
 Utilizzare il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Il documento di origine.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/P3gaA34.png)

To export VSD diagram to XPS:

1. Creare un'istanza della classe Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.

L'immagine seguente mostra il file di output XPS.

**The output XPS.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/1ESRxSy.png)
### **Exporting to XPS Programming Sample**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXPS.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir+ "ExportToXPS.vsd");

// Save as XPS
diagram.save(dataDir + "ExportToXPS_Out.xps", SaveFileFormat.XPS);

{{< /highlight >}}
```
## **Exporting a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizzare il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

To export VSD diagram to SVG, perform the following steps:

1. Creare un'istanza della classe Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Exporting Diagram to SVG Programming Sample**
The code samples show how to export a diagram to SVG using Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToSVG.class);

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save as SVG
diagram.save(dataDir+ "ExportToSVG_Out.svg", SaveFileFormat.SVG);

{{< /highlight >}}
```
## **Exporting a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizzare il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

Per esportare un VSD da diagram a XAML:

1. Creare un'istanza della classe Diagram.
1. Call the class' Save method and set XAML as the export format.
### **Exporting to XAML Programming Sample**
The code sample show how to export a diagram to XAML using Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXAML.class); 

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");

// save as XAML
diagram.save(dataDir + "ExportToXAML_Out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}
```

## **Converti Visio Disegno con forme selettive**
Utilizzando Aspose.Diagram API, gli sviluppatori possono selezionare un gruppo di forme per convertire un disegno Visio in qualsiasi altro formato supportato. La classe RenderingSaveOptions offre un membro Shapes per mantenere il gruppo di forme. Ogni classe di opzione di salvataggio è la forma estesa della classe RenderingSaveOptions.

Per esportare un disegno Visio con forme selettive:

1. Creare un'istanza della classe Diagram.
1. Crea un'istanza di qualsiasi classe SaveOption per specificare le impostazioni come descritto qui:[Specificare Visio Opzioni di salvataggio](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. Chiamare il metodo save dell'oggetto classe Diagram e passare l'oggetto classe opzione save come parametro.
### **Conversione Visio Disegno con esempio di programmazione di forme selettive**
L'esempio di codice mostra come esportare un disegno con forme Visio selettive.

```
{{< highlight "java" >}}
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
```