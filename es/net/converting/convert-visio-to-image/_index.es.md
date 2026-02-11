---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportar diagramas a formatos de archivo de imagen**
 Este artículo explica cómo exportar un Microsoft Visio diagram a una imagen usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API. Utilice el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) constructor de clase para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.
### **Exportar Microsoft Visio Dibujo a archivo de imagen**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}
```

También es posible guardar una página en particular en la imagen, en lugar de todo el documento:

```
{{< highlight "csharp" >}}
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
```