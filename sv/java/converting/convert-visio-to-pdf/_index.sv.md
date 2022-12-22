---
title:  Konvertera Visio till PDF format
linktitle: Konvertera Visio till PDF
type: docs
weight: 10
url: /sv/java/convert-visio-to-pdf/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till PDF format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM.
---
## **Exporterar till PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java skriver direkt informationen om API och versionsnumret i utgående dokument. Till exempel, när en ritning renderas till PDF, fylls Aspose.Diagram for Java**Ansökan**fält med värdet 'Aspose.Diagram' och**PDF Producent**fält med ett värde, t.ex. 'Aspose.Diagram 17.9'.

Observera att du inte kan instruera Aspose.Diagram for Java API att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}}

 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till PDF med[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Använd[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Källfilen.**

![todo:image_alt_text](how-to-convert-a-visio-diagram_1.png)

Så här exporterar du VSD diagram till PDF:

1. Skapa en instans av klassen Diagram.
1. Anropa Diagram classs Save-metoden och ställ in utdataformatet till PDF.

Nedan finns en bild av utdatafilen PDF.

**Utdatafilen PDF.**

![todo:image_alt_text](how-to-convert-a-visio-diagram_2.png)
### **Exporterar till PDF Programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Dela flera sidor**
Aspose.Diagram for Java tillåter uppdelning av flera sidor samtidigt som Microsoft Visio Diagram Diagram Diagram konverteras till PDF. Följande kodavsnitt visar funktionen.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Använd Page Save Callback**
Om du har flera sidor tillåter Aspose.Diagram for Java att använda sidsparande återuppringning samtidigt som du konverterar Microsoft Visio Diagram till PDF. Följande kodavsnitt visar funktionaliteten.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **TestDiagramPageSavingCallback Class**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
