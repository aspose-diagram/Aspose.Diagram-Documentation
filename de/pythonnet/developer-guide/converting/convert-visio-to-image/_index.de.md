---
title:  Konvertieren Sie Visio in Bildformate
linktitle: Konvertieren Sie Visio in Bilder
type: docs
weight: 20
url: /de/python-net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Diagramme in Bilddateiformate exportieren**
 In diesem Artikel wird erläutert, wie Sie ein Microsoft Visio diagram mithilfe von in ein Bild exportieren[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Verwenden Sie den Klassenkonstruktor [Diagram], um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

So exportieren Sie eine diagram in ein Bild:

- Erstellen Sie eine Instanz der Klasse Diagram.
- Rufen Sie die Save-Methode der Diagram-Klasse auf und legen Sie das Bildformat fest, in das Sie exportieren möchten. Die Ausgabebilddatei sieht aus wie die Originaldatei.
### **Microsoft Visio Zeichnung in Bilddatei exportieren**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


Es ist auch möglich, anstelle des gesamten Dokuments eine bestimmte Seite als Bild zu speichern:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}
