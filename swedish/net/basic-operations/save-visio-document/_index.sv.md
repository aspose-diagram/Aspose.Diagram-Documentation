---
title: Spara Visio dokument programmatiskt
linktitle: Spara Visio dokument
type: docs
weight: 30
url: /sv/net/save-visio-document/
description: Den här sidan beskriver hur man sparar Visio dokument till fil, streama med Aspose.Diagram bibliotek.
---
## **Visio Ritning Spara Översikt**
 Använd[Diagram.Save]() metod för att spara en Microsoft Visio ritning. Det finns överbelastningar som gör det möjligt att spara en ritning till fil. Ritningen kan sparas i valfritt sparformat som stöds av Aspose.Diagram. För listan över alla sparade format som stöds, se[SaveFileFormat]() Enum.
## **Sparar Visio Diagram**
 Klassen Diagram i Aspose.Diagram API representerar en Visio-ritning och utvecklare kan spara dess Visio diagram-objekt i vilket filformat som helst. För att spara en Microsoft Visio fil, använd helt enkelt[Diagram.Save]()metod, accepterar den ett filnamn med en fullständig sökväg eller ett filströmsobjekt. Aspose.Diagram API härleder sparaformatet från filtillägget och erbjuder även en extra SaveFileFormat-parameter för att specificera utdatafilformatet.
### **Spara ett Visio Diagram i valfritt filformat som stöds**
Genom att använda Aspose.Diagram API kan utvecklare spara en Visio diagram i vilket filformat som helst som stöds enligt listan nedan:
**VSDX, VSDM.**
### **Sparar Diagram Programmeringsexempel**
Exemplet nedan sparar ett dokument till en fil.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Ange Visio Spara alternativ**
 Det finns flera[Diagram.Save]() metodöverbelastningar som accepterar ett SaveOptions-objekt. Detta bör vara ett objekt av en klass som härrör från klassen SaveOptions. Varje sparaformat har en motsvarande klass som innehåller sparaalternativ för det sparade formatet. Det finns till exempel PdfSaveOptions för sparaformatet SaveFileFormat.PDF.
### **Visio Diagram Spara alternativ**
Dessa exempel visar hur man:

- [Använd Diagram Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd PDF-sparalternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd HTML-sparaalternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd alternativ för bildspar](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd SVG Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Använd SWF-sparalternativ](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Användning av Diagram Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **Användning av PDF-sparalternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i ett PDF-format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **Användning av HTML-sparaalternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i HTML-filformat.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **Användning av bildsparalternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i bildfilformat.



{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


Användning av SVG Spara alternativ

Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i SVG-format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


Användning av SWF-sparalternativ

Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i SWF-format.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

Ibland behöver utvecklare spara eller exportera Visio-diagram till olika filformat programmatiskt (som VDX, PDF, JPEG och så vidare).
## **Spara VSD-filen till olika filformat (VDX, PDF och JPEG)**
 Den här artikeln ger ett kodexempel som illustrerar hur du använder[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) och[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) för att spara en Microsoft Visio VSD-fil till en VDX-fil, PDF-fil eller en JPEG-fil programmatiskt. Nedan finns parallella kodavsnitt för VSTO och Aspose.Diagram for .NET som förklarar hur man sparar en VSD-fil i olika filformat. Du kommer att märka att Aspose.Diagram-koden är kortare. Använd gärna koden och ändra den för att möta dina specifika behov.
### **Spara en VSD-fil till andra format med VSTO**
VSTO låter dig programmera med Microsoft Visio filer. Så här sparar du en fil i andra format:

1. Skapa ett Visio applikationsobjekt.
1. Gör applikationsobjektet osynligt.
1. Ladda diagram.
1. Spara till VDX, PDF och JPEG.
1. Avsluta applikationsobjektet Visio.
#### **Spara en VSD-fil med VSTO-programmeringsexempel**
{{% alert color="primary" %}} 

använder Visio = Microsoft.Office.Interop.Visio;
Importer Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Exempel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withVSTO-SaveDiagramTo_VDX_PDF_JPEG_withVSTO.cs" >}}
### ` `**Spara VSD-fil till andra format med Aspose.Diagram for .NET**
Med Aspose.Diagram behöver utvecklare inte Microsoft Office Visio i maskinen, och de kan arbeta oberoende av Microsoft Office Automation.

Kodavsnitten nedan visar hur man:

1. Ladda ett diagram.
1. Spara diagram till VSX, PDF och JPEG.
#### **Sparar VSD Fil med Aspose.Diagram for .NET Programmeringsexempel**
{{% alert color="primary" %}} 

använder Aspose.Diagram;
Importer Aspose.Diagram

{{% /alert %}} 

**Exempel:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
