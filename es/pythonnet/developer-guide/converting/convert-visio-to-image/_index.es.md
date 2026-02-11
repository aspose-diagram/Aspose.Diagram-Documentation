---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/python-net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportar diagramas a formatos de archivo de imagen**
 Este artículo explica cómo exportar un Microsoft Visio diagram a una imagen usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Use el constructor de clase [Diagram] para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.
### **Exportar Microsoft Visio Dibujo a archivo de imagen**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


También es posible guardar una página en particular en la imagen, en lugar de todo el documento:


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
