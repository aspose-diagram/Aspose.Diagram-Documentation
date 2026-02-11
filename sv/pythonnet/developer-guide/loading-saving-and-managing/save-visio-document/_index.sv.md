---
title: Spara Visio dokument programmatiskt
linktitle: Spara Visio dokument
type: docs
weight: 30
url: /sv/python-net/save-visio-document/
description: Den här sidan beskriver hur man sparar Visio dokument till fil, streama med Aspose.Diagram bibliotek.
---
## **Visio Ritning Spara Översikt**
 Använd[Diagram.Save]() metod för att spara en Microsoft Visio ritning. Det finns överbelastningar som gör det möjligt att spara en ritning till fil. Ritningen kan sparas i valfritt sparformat som stöds av Aspose.Diagram. För listan över alla sparade format som stöds, se[SaveFileFormat]() Enum.
## **Sparar Visio Diagram**
 Klassen Diagram i Aspose.Diagram API representerar en Visio-ritning och utvecklare kan spara dess Visio diagram-objekt i vilket filformat som helst. För att spara en Microsoft Visio fil, använd helt enkelt[Diagram.Save]()metod, accepterar den ett filnamn med en fullständig sökväg eller ett filströmsobjekt. Aspose.Diagram API härleder sparaformatet från filtillägget och erbjuder även en extra SaveFileFormat-parameter för att specificera utdatafilformatet.
### **Spara ett Visio Diagram i valfritt filformat som stöds**
Genom att använda Aspose.Diagram API kan utvecklare spara en Visio diagram i vilket filformat som helst som stöds enligt listan nedan:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Sparar Diagram Programmeringsexempel**
Exemplet nedan sparar ett dokument till en fil.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Ange Visio Spara alternativ**
 Det finns flera[Diagram.Save]()metodöverbelastningar som accepterar ett SaveOptions-objekt. Detta bör vara ett objekt av en klass som härrör från klassen SaveOptions. Varje sparaformat har en motsvarande klass som innehåller sparaalternativ för det sparade formatet. Det finns till exempel PdfSaveOptions för sparaformatet SaveFileFormat.PDF.
### **Visio Diagram Spara alternativ**
Dessa exempel visar hur man:

- [Använd Diagram Spara alternativ](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Använd PDF Spara alternativ](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Använd HTML Spara alternativ](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Använd alternativ för bildspar](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Använd SVG Spara alternativ](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Använd SWF Spara alternativ](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Användning av Diagram Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet Visio.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.DiagramSaveOptions(SaveFileFormat.VSDX)

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", options)
{{< /highlight >}}




#### **Användning av PDF Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet PDF.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.PdfSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the pdf format
diagram.save("CreateNewVisio_out.pdf", options)
{{< /highlight >}}




#### **Användning av HTML Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument till filformatet HTML.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.HTMLSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the html format
diagram.save("Visio_out.html", options)
{{< /highlight >}}




#### **Användning av bildsparalternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i bildfilformat.




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



Användning av SVG Spara alternativ

Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet SVG.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as svg
options = saving.SVGSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the svg format
diagram.save("ExportPageToSvg_out.svg", options)
{{< /highlight >}}


Ibland behöver utvecklare spara eller exportera Visio-diagram till olika filformat programmatiskt (som VDX, PDF, JPEG och så vidare).

### ` `**Sparar VSD fil till andra format med Aspose.Diagram för Python via .NET**
Med Aspose.Diagram behöver utvecklare inte Microsoft Office Visio i maskinen, och de kan arbeta oberoende av Microsoft Office Automation.

Kodavsnitten nedan visar hur man:

1. Ladda ett diagram.
1. Spara diagram till VSX, PDF och JPEG.
#### **Sparar VSD Fil med Aspose.Diagram för Python via .NET Programmeringsexempel**
{{% alert color="primary" %}} 

import aspose.diagram
från aspose.diagram import *

{{% /alert %}} 

**Exempel:**


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save the diagram as VDX
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToVDXwithAspose_out.vdx"), SaveFileFormat.VDX)

#// Save as PDF
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToPDFwithAspose_out.pdf"), SaveFileFormat.PDF)

#// Save as JPEG
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToJPGwithAspose_out.jpg"), SaveFileFormat.JPEG)
{{< /highlight >}}

