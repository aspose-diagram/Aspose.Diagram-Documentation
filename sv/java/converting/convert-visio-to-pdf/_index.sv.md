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

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToPDF.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

// Save as PDF file format
diagram.save(dataDir + "ExportToPDF_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}

### **Dela flera sidor**
Aspose.Diagram for Java tillåter uppdelning av flera sidor samtidigt som Microsoft Visio Diagram Diagram Diagram konverteras till PDF. Följande kodavsnitt visar funktionen.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UsePDFSaveOptions.class);      
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Network Diagram_start.vsdx");
// Options when saving a diagram into the PDF format
PdfSaveOptions options = new PdfSaveOptions();
// set SplitMultiPages option
options.setSplitMultiPages(true);
// save in PDF format
diagram.save(dataDir + "SplitMultiPages.pdf", options);

{{< /highlight >}}

### **Använd Page Save Callback**
Om du har flera sidor tillåter Aspose.Diagram for Java att använda sidsparande återuppringning samtidigt som du konverterar Microsoft Visio Diagram till PDF. Följande kodavsnitt visar funktionaliteten.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DocumentConversionProgress.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
PdfSaveOptions options = new PdfSaveOptions();
          
//set page saving call back
options.setPageSavingCallback( new TestDiagramPageSavingCallback());

// save Visio drawing
diagram.save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}


#### **TestDiagramPageSavingCallback Class**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
import com.aspose.diagram.IPageSavingCallback;
import com.aspose.diagram.PageEndSavingArgs;
import com.aspose.diagram.PageStartSavingArgs;

public class TestDiagramPageSavingCallback implements IPageSavingCallback
{
    public void pageStartSaving(PageStartSavingArgs args)
    {
    	System.out.println("Start saving page index " + args.getPageIndex() + " of pages " + args.getPageCount());
    }

    public void pageEndSaving(PageEndSavingArgs args)
    {
    	System.out.println("End saving page index " + args.getPageIndex() + " of pages " + args.getPageCount());

        //don't output pages after page index 8.
        if (args.getPageIndex() >= 8)
        {
            args.setHasMorePages(false);
        }
    }
}


{{< /highlight >}}

