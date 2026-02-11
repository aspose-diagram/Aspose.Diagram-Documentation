---
title: Convert Visio to Images formats 
linktitle: Convert Visio to Images
type: docs
weight: 20
url: /net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---

## **Export Diagrams to Image File Formats**
This article explains how to export a Microsoft Visio diagram to an image using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API. Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export a diagram to an image:

- Create an instance of the Diagram class.
- Call the Diagram class' Save method and set the image format you want to export to.The output image file looks like the original file.
### **Export Microsoft Visio Drawing to Image File**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


It is also possible to save a particular page to image, instead of the entire document:


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
