---
title:  Converti Visio in formati Immagini
linktitle: Converti Visio in immagini
type: docs
weight: 20
url: /it/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Esportazione di diagrammi in formati di file immagine**
This article explains how to export a Microsoft Visio diagram to an image using Aspose.Diagram for Python via Java.

Use the Diagram class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**[Il file VSD di esempio.](ExportToImage.vsd)**

Per esportare un diagram in un'immagine:

- Creare un'istanza della classe Diagram.
- Chiama il metodo Save della classe Diagram e imposta il formato dell'immagine in cui desideri esportare. Il file dell'immagine di output ha l'aspetto del file originale.

**Il file di output PNG.**

![cose da fare:immagine_alt_testo](ExportToImage.png)
### **Esempio di programmazione dell'esportazione in un file immagine**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToImage.vsd")

# Save as PNG
diagram.save("ExportToImage_Out.png", SaveFileFormat.PNG)

jpype.shutdownJVM()

{{< /highlight >}}


È anche possibile salvare una pagina particolare come immagine, invece dell'intero documento:


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("ExportToImage.vsd")

# Save diagram as PNG
options = ImageSaveOptions(SaveFileFormat.PNG)

# Save one page only, by page index
options.setPageIndex(0)

# Save resultant Image file
diagram.save("ExportPageToImage_Out.png", options)

jpype.shutdownJVM()

{{< /highlight >}}
