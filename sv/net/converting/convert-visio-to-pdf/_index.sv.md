---
title:  Konvertera Visio till PDF format
linktitle: Konvertera Visio till PDF
type: docs
weight: 10
url: /sv/net/convert-visio-to-pdf/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till PDF format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM.
---
## **Exportera till PDF**
{{% alert color="primary" %}}

 Aspose.Diagram for .NET skriver direkt informationen om API och versionsnumret i utgående dokument. Till exempel, när en ritning renderas till PDF, fylls Aspose.Diagram for .NET**Ansökan** fält med värdet 'Aspose.Diagram' och**PDF Producent** fält med värde, t.ex. 'Aspose.Diagram 17,9'.

Observera att du inte kan instruera Aspose.Diagram for .NET API att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}}

 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till PDF med[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Använd[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klasskonstruktorn för att läsa diagram-filerna och metoden Spara för att exportera diagram till valfritt bildformat som stöds.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Källfilen.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_1.png)|


Så här exporterar du VSD diagram till PDF:

1. Skapa en instans av klassen Diagram.
1. Anropa Diagram classs Save-metoden och ställ in utdataformatet till PDF.

Nedan finns en bild av utdatafilen PDF.

|**Utdatafilen PDF.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_2.png)|
### **Exportera Microsoft Visio Ritning till PDF**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till PDF med C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}
```
### **Dela flera sidor**
Aspose.Diagram for .NET tillåter uppdelning av flera sidor samtidigt som Microsoft Visio Diagram Diagram Diagram konverteras till PDF. Följande kodavsnitt visar funktionen.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Network Diagram_start.vsdx");
// Initialize PdfSaveOptions
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
// set SplitMultiPages option
options.SplitMultiPages = true;
// save in PDF format
diagram.Save(dataDir + "SplitMultiPages.pdf", options);

{{< /highlight >}}
```
### **Använd Page Save Callback**
Om du har flera sidor tillåter Aspose.Diagram for .NET att använda sidsparande återuppringning samtidigt som du konverterar Microsoft Visio Diagram till PDF. Följande kodavsnitt visar funktionaliteten.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Network Diagram_start.vsdx");
// Initialize PdfSaveOptions
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
// set PageSavingCallback option
options.PageSavingCallback = new TestDiagramPageSavingCallback();
// save in PDF format
diagram.Save(dataDir + "PageSavingCallback.pdf", options);

{{< /highlight >}}
```
#### **TestDiagramPageSavingCallback Class**
{{< highlight "java" >}}

 public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{
 
 public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
 
 {
 
 Console.WriteLine("Börja spara {1} sida 0,0,0,0,1,0,1,0,1,0,0,0 
 }
 
 public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
 
 {
 
 Console.Skriv sida av {0}s. 1 sida,P 1 s, 1 s, 1 s, 1 s, 1 s, 1 s. 
 
 // matar inte ut sidor efter sida index 8.
 
 if (args.pageIndex> = 8) 
 
 {
 
 args.hasmorePages = falsk; 
 

