---
title:  Converti Visio in formati Immagini
linktitle: Converti Visio in immagini
type: docs
weight: 20
url: /it/net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Esporta diagrammi in formati di file immagine**
 Questo articolo spiega come esportare un Microsoft Visio diagram in un'immagine utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API. Usa il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) costruttore di classe per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

Per esportare un diagram in un'immagine:

- Creare un'istanza della classe Diagram.
- Chiama il metodo Save della classe Diagram e imposta il formato dell'immagine in cui desideri esportare. Il file dell'immagine di output ha l'aspetto del file originale.
### **Esporta Microsoft Visio Disegno su file immagine**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


È anche possibile salvare una pagina particolare come immagine, invece dell'intero documento:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportPageToImage.vsd");

// Save diagram as PNG
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.PNG);

// Save one page only, by page index
options.PageIndex = 0;

// Save resultant Image file
diagram.Save(dataDir + "ExportPageToImage_out.png", options);

{{< /highlight >}}
