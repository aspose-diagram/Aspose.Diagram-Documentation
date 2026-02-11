---
title:  Konvertieren Sie Visio in Bildformate
linktitle: Konvertieren Sie Visio in Bilder
type: docs
weight: 20
url: /de/java/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Diagramme in Bilddateiformate exportieren**
 In diesem Artikel wird erläutert, wie Sie ein Microsoft Visio diagram mithilfe von in ein Bild exportieren[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Verwenden Sie die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.
**Die Quelldatei. Beachten Sie, dass die Pfeil- und Dreiecksbeschriftungen fett gedruckt sind.**

![todo: Bild_alt_Text](http://i.imgur.com/WOV36ek.png)

So exportieren Sie eine diagram in ein Bild:

- Erstellen Sie eine Instanz der Klasse Diagram.
- Rufen Sie die Save-Methode der Diagram-Klasse auf und legen Sie das Bildformat fest, in das Sie exportieren möchten. Die Ausgabebilddatei sieht aus wie die Originaldatei.

**Die Ausgabedatei PNG.**

![todo: Bild_alt_Text](http://i.imgur.com/WOV36ek.png)
### **Exportieren in eine Bilddatei Programmierbeispiel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToImage.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save as PNG
diagram.save(dataDir+ "ExportToImage_Out.png", SaveFileFormat.PNG);

{{< /highlight >}}


Es ist auch möglich, anstelle des gesamten Dokuments eine bestimmte Seite als Bild zu speichern:


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
