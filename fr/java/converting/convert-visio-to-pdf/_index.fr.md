---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /fr/java/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Exporting to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for Java populates **Application**champ avec la valeur 'Aspose.Diagram' et**PDF Producer**champ avec une valeur, par exemple 'Aspose.Diagram 17.9'.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram for Java API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Le fichier sources.**

![tâche : image_autre_texte](how-to-convert-a-visio-diagram_1.png)

To export VSD diagram to PDF:

1. Créez une instance de la classe Diagram.
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

**Le fichier de sortie PDF.**

![tâche : image_autre_texte](how-to-convert-a-visio-diagram_2.png)
### **Exporting to PDF Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToPDF.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

// Save as PDF file format
diagram.save(dataDir + "ExportToPDF_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}

### **Fractionner plusieurs pages**
Aspose.Diagram for Java allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  


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

### **Utiliser le rappel d'enregistrement de page**
In case you have multiple pages, Aspose.Diagram for Java allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  


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


#### **Classe TestDiagramPageSavingCallbackTestDiagramPageSavingCallback Class**

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

