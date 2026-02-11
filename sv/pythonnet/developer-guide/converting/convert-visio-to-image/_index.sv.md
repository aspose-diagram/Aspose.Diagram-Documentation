---
title:  Konvertera Visio till bildformat
linktitle: Konvertera Visio till bilder
type: docs
weight: 20
url: /sv/python-net/convert-visio-to-image/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till olika bildformat. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportera diagram till bildfilformat**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till en bild med[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Använd klasskonstruktorn [Diagram] för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds.

Så här exporterar du ett diagram till en bild:

- Skapa en instans av klassen Diagram.
- Anropa Diagram-klassens Spara-metod och ställ in bildformatet du vill exportera till. Utdatafilen ser ut som originalfilen.
### **Exportera Microsoft Visio Ritning till bildfil**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


Det är också möjligt att spara en viss sida till bild istället för hela dokumentet:


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
