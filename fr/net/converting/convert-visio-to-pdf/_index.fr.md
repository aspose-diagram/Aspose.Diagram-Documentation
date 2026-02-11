---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /fr/net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Application** champ avec la valeur 'Aspose.Diagram' et**PDF Producer** champ avec valeur, par exemple 'Aspose.Diagram 17.9'.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram for .NET API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Utilisez le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) constructeur de classe pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Le fichier sources.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_1.png)|


To export VSD diagram to PDF:

1. Créez une instance de la classe Diagram.
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

|**Le fichier de sortie PDF.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_2.png)|
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.


{{< highlight csharp >}}
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

### **Fractionner plusieurs pages**
Aspose.Diagram for .NET allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  


{{< highlight csharp >}}
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

### **Utiliser le rappel d'enregistrement de page**
In case you have multiple pages, Aspose.Diagram for .NET allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  


{{< highlight csharp >}}
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

#### **Classe TestDiagramPageSavingCallbackTestDiagramPageSavingCallback Class**
{{< highlight "java" >}}

 classe publique TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback


 }
 
 public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
 
 {
 
 Console.WriteLine("Fin de l'enregistrement diagram page {0} de pages {1}", Index + args.Pageargs1); 
 
 // ne pas sortir pages après l'index de page 8.
 
 if (args.pageindex> = 8) 
 
 {
 
 args.hasmorepages = false; 
 
} 
 
 
} 
 
 _x000.
