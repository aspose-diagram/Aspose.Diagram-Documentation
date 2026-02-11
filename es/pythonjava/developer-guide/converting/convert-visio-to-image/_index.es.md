---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportación de diagramas a formatos de archivo de imagen**
This article explains how to export a Microsoft Visio diagram to an image using Aspose.Diagram for Python via Java.

Use the Diagram class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**[El archivo de ejemplo VSD.](ExportToImage.vsd)**

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.

**El archivo de salida PNG.**

![todo:imagen_alternativa_texto](ExportToImage.png)
### **Ejemplo de programación de exportación a archivo de imagen**

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


También es posible guardar una página en particular en la imagen, en lugar de todo el documento:


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
