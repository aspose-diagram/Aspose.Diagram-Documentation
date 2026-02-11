---
title:  Konvertera Visio till PDF format
linktitle: Konvertera Visio till PDF
type: docs
weight: 10
url: /sv/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Exporterar till PDF**
{{% alert color="primary" %}}

Aspose.Diagram för Python via Java skriver direkt informationen om API och versionsnumret i utgående dokument. Till exempel, när en ritning renderas till PDF, fylls Aspose.Diagram for Java**Ansökan**fält med värdet 'Aspose.Diagram' och**PDF Producent**fält med ett värde, t.ex. 'Aspose.Diagram 17.9'.

Observera att du inte kan instruera Aspose.Diagram för Python via Java att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}}

Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till PDF med Aspose.Diagram för Python via Java.

Använd Diagram-klassens konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

[VSD diagram](ExportToPDF.vsd)är exemplet på ritningsfilen för att exportera PDF. Du kan använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, 78163481, 7816, 7816, 7816, 7816, 4016, 7816, 7816, 7816, 7816, 76123481, 76133481, VDX, VST, VSTX, 7816, 7816, 7816, 716.

Så här exporterar du VSD diagram till PDF:

1. Skapa en instans av klassen Diagram.
1. Anropa Diagram classs Save-metoden och ställ in utdataformatet till PDF.

### **Exporterar till PDF Programmeringsexempel**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToPDF.vsd")

# Save as PDF file format
diagram.save("ExportToPDF_Out.pdf", SaveFileFormat.PDF)

jpype.shutdownJVM()

{{< /highlight >}}


### **Dela flera sidor**
Aspose.Diagram for Java tillåter uppdelning av flera sidor samtidigt som Microsoft Visio Diagram Diagram Diagram konverteras till PDF. Följande kodavsnitt visar funktionen.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("Network Diagram_start.vsdx")
# Options when saving a diagram into the PDF format
options = PdfSaveOptions()
# set SplitMultiPages option
options.setSplitMultiPages(True)
# save in PDF format
diagram.save("SplitMultiPages.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}

