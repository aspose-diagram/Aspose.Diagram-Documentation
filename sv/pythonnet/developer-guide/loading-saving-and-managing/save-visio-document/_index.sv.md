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

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseDiagramSaveOptions.py" >}}



#### **Användning av PDF Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet PDF.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UsePdfSaveOptions.py" >}}



#### **Användning av HTML Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument till filformatet HTML.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseHtmlSaveOptions.py" >}}



#### **Användning av bildsparalternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i bildfilformat.



{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseImageSaveOptions.py" >}}


Användning av SVG Spara alternativ

Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet SVG.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseSvgSaveOptions.py" >}}

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

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-SaveDiagramTo_VDX_PDF_JPEG_withAspose.py" >}}
