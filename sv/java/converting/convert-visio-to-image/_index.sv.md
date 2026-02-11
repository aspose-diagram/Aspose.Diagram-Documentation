---
title:  Konvertera Visio till bildformat
linktitle: Konvertera Visio till bilder
type: docs
weight: 20
url: /sv/java/convert-visio-to-image/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till olika bildformat. Konvertera Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,0761 PNG, JPEG a, BMP-linjer med några få linjer med kod.
---
## **Exportera diagram till bildfilformat**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till en bild med[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Använd[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class' konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds. Bilden nedan visar en VSD-fil som håller på att sparas i PNG-format. Du kan också använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, 0761101 eller 13371) också.
**Källfilen. Observera att pil- och triangeletiketterna är i fetstil.**

![todo:image_alt_text](http://i.imgur.com/WOV36ek.png)

Så här exporterar du ett diagram till en bild:

- Skapa en instans av klassen Diagram.
- Anropa Diagram-klassens Spara-metod och ställ in bildformatet du vill exportera till. Utdatafilen ser ut som originalfilen.

**Utdata-PNG-filen.**

![todo:image_alt_text](http://i.imgur.com/WOV36ek.png)
### **Exportera till bildfil Programmeringsexempel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToImage.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save as PNG
diagram.save(dataDir+ "ExportToImage_Out.png", SaveFileFormat.PNG);

{{< /highlight >}}


Det är också möjligt att spara en viss sida till bild istället för hela dokumentet:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportPageToImage.class);     
// load diagram
Diagram diagram = new Diagram(dataDir + "ExportPageToImage.vsd");

//Save diagram as PNG
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.PNG);

// Save one page only, by page index
options.setPageIndex(0);

//Save resultant Image file
diagram.save(dataDir + "ExportPageToImage_Out.png", options);

{{< /highlight >}}
