---
title: Spara Visio dokument programmatiskt
linktitle: Spara Visio dokument
type: docs
weight: 30
url: /sv/java/save-visio-document/
description: Den här sidan beskriver hur man sparar Visio dokument till fil, streama med Aspose.Diagram bibliotek.
---
## **Visio Ritning Spara Översikt**
 Använd[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) metod för att spara en Microsoft Visio ritning. Det finns överbelastningar som gör det möjligt att spara en ritning till fil. Ritningen kan sparas i valfritt sparformat som stöds av Aspose.Diagram. För listan över alla sparade format som stöds, se[SaveFileFormat](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat) Enum.
## **Sparar Visio Diagram**
 Klassen Diagram i Aspose.Diagram API representerar en Visio-ritning och utvecklare kan spara dess Visio diagram-objekt i vilket filformat som helst. För att spara en Microsoft Visio fil, använd helt enkelt[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\))-metoden, accepterar den ett filnamn med den fullständiga sökvägen eller ett filströmsobjekt. Aspose.Diagram API härleder sparaformatet från filtillägget och erbjuder även en extra SaveFileFormat-parameter för att ange utdatafilformat.
### **Spara ett Visio Diagram i valfritt filformat som stöds**
Genom att använda Aspose.Diagram API kan utvecklare spara en Visio diagram i vilket filformat som helst som stöds enligt listan nedan:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Sparar Diagram Programmeringsexempel**
Exemplet nedan sparar ett dokument till en fil.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Ange Visio Spara alternativ**
 Det finns flera[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)metodöverbelastningar som accepterar ett SaveOptions-objekt. Detta bör vara ett objekt av en klass som härrör från klassen SaveOptions. Varje spara-format har en motsvarande klass som innehåller spara-alternativ för det spara-formatet, till exempel finns det PdfSaveOptions för SaveFileFormat.PDF spara-format.
### **Visio Diagram Spara alternativ**
Dessa exempel visar hur man:

- [Använd Diagram Spara alternativ](/diagram/sv/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Använd PDF Spara alternativ](/diagram/sv/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Använd HTML Spara alternativ](/diagram/sv/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Använd alternativ för bildspar](/diagram/sv/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Använd SVG Spara alternativ](/diagram/sv/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Användning av Diagram Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Användning av PDF Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet PDF.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Användning av HTML Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet HTML.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Användning av bildsparalternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i ett bildformat.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Användning av SVG Spara alternativ**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett dokument i formatet SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
