---
title:  Konvertera Visio till bildformat
linktitle: Konvertera Visio till bilder
type: docs
weight: 20
url: /sv/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a några rader kod.
---
## **Exportera diagram till bildfilformat**
Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till en bild med Aspose.Diagram för Python via Java.

Använd Diagram-klassens konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds. Bilden nedan visar en VSD-fil som håller på att sparas till PNG-format. Du kan använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, 0761113476, 0761130476, 0761130476, 0761130476, 0761130476, 376113416 och 376113476)

**[Exempelfilen VSD.](ExportToImage.vsd)**

Så här exporterar du ett diagram till en bild:

- Skapa en instans av klassen Diagram.
- Anropa Diagram-klassens Spara-metod och ställ in bildformatet du vill exportera till. Utdatafilen ser ut som originalfilen.

**Utdatafilen PNG.**

![todo:image_alt_text](ExportToImage.png)
### **Exportera till bildfil Programmeringsexempel**

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


Det är också möjligt att spara en viss sida till bild istället för hela dokumentet:


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
