---
title: Convert Visio to Images formats 
linktitle: Convert Visio to Images
type: docs
weight: 20
url: /python-net/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---

## **Export Diagrams to Image File Formats**
This article explains how to export a Microsoft Visio diagram to an image using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Use the [Diagram]class constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export a diagram to an image:

- Create an instance of the Diagram class.
- Call the Diagram class' Save method and set the image format you want to export to.The output image file looks like the original file.
### **Export Microsoft Visio Drawing to Image File**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


It is also possible to save a particular page to image, instead of the entire document:


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
