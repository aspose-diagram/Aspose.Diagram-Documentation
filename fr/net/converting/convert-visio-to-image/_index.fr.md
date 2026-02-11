---
title:  Convertir Visio en formats Images
linktitle: Convertir Visio en Images
type: docs
weight: 20
url: /fr/net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exporter des diagrammes vers des formats de fichier image**
 Cet article explique comment exporter un Microsoft Visio diagram vers une image en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API. Utilisez le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) constructeur de classe pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Pour exporter un diagram vers une image :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram et définissez le format d'image vers lequel vous souhaitez exporter. Le fichier image de sortie ressemble au fichier d'origine.
### **Exporter Microsoft Visio Dessin vers un fichier image**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


Il est également possible d'enregistrer une page particulière dans l'image, au lieu du document entier :


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
