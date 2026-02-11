---
title:  Konvertera Visio till bildformat
linktitle: Konvertera Visio till bilder
type: docs
weight: 20
url: /sv/net/convert-visio-to-image/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till olika bildformat. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportera diagram till bildfilformat**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till en bild med[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API. Använd[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klasskonstruktorn för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds.

Så här exporterar du ett diagram till en bild:

- Skapa en instans av klassen Diagram.
- Anropa Diagram-klassens Spara-metod och ställ in bildformatet du vill exportera till. Utdatafilen ser ut som originalfilen.
### **Exportera Microsoft Visio Ritning till bildfil**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


Det är också möjligt att spara en viss sida till bild istället för hela dokumentet:


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
