---
title:  Konvertera Visio till PDF-format
linktitle: Konvertera Visio till PDF
type: docs
weight: 10
url: /sv/net/convert-visio-to-pdf/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till PDF-format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM till PDF med några rader kod.
---
## **Exportera till PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET skriver direkt informationen om API och versionsnumret i utgående dokument. Till exempel, när en ritning renderas till PDF, fylls Aspose.Diagram for .NET**Ansökan** fält med värdet 'Aspose.Diagram' och**PDF-producent** fält med värde, t.ex. 'Aspose.Diagram 17,9'.

Observera att du inte kan instruera Aspose.Diagram for .NET API att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}}

 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till PDF med[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Använd[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klasskonstruktorn för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds.

Bilden nedan visar VSD diagram som kodavsnitten nedan exporterar PDF. Du kan också använda andra diagram-format (VSS, VSSM, VDX, VST, VSTX, VDX, VTX eller VSX).

|**Källfilen.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_1.png)|


För att exportera VSD diagram till PDF:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram klasser Spara metoden och ställ in utdataformatet till PDF.

Nedan finns en bild av den utgående PDF-filen.

|**Utdata-PDF-filen.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_2.png)|
### **Exportera Microsoft Visio Ritning till PDF**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till PDF med C#.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Dela flera sidor**
Aspose.Diagram for .NET tillåter att dela flera sidor samtidigt som Microsoft Visio Diagram konverteras till PDF. Följande kodavsnitt visar funktionaliteten.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Använd Page Save Callback**
Om du har flera sidor tillåter Aspose.Diagram for .NET att använda sidsparande återuppringning samtidigt som du konverterar Microsoft Visio Diagram till PDF. Följande kodavsnitt visar funktionaliteten.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **TestDiagramPageSavingCallback Class**
{{< highlight "java" >}}

 public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{  public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)  {  Console.WriteLine("Börja spara {1} sida 0,0,0,0,1,0,1,0,1,0,0,0  }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.Skriv sida av {0}s. 1 sida,P 1 s, 1 s, 1 s, 1 s, 1 s, 1 s.   // matar inte ut sidor efter sida index 8.  if (args.pageIndex> = 8)   {  args.hasmorePages = falsk;  
