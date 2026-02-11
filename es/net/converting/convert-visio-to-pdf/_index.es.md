---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /es/net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Solicitud** campo con valor 'Aspose.Diagram' y**PDF Producer** campo con valor, por ejemplo, 'Aspose.Diagram 17.9'.

Tenga en cuenta que no puede indicar al Aspose.Diagram for .NET API que cambie o elimine esta información de los documentos de salida.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Utilizar el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) constructor de clase para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**El archivo fuente.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_1.png)|


To export VSD diagram to PDF:

1. Cree una instancia de la clase Diagram.
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

|**El archivo de salida PDF.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_2.png)|
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.

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
### **Dividir varias páginas**
Aspose.Diagram for .NET allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

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
### **Usar página Guardar devolución de llamada**
In case you have multiple pages, Aspose.Diagram for .NET allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

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
#### **Clase TestDiagramPageSavingCallback**
{{< highlight "java" >}}

 TestDiagramPageSavingCallback de clase pública: Aspose.Diagram.Saving.IPageSavingCallback

{
 
 public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
 
 {
 
 Console.WriteLine("Empezar a guardar diagram página {0} de las páginas {1}", args.PageIndex + 0Page_dgs, args.PageIndex + 0.Count_d); 
 }
 
 public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
 
 {
 
 Console.WriteLine("Finalizar guardado diagram página {0} de páginas {1}", Pageardex 1., Pageardex 1.); 
 
 //don't output pages after page index 8.
 
 if (args.PageIndex >= 8)
 
 {
 
 args.HasMorePages = false;
 
 }
 
 }
 
 }
