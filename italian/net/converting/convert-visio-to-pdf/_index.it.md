﻿---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /it/net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Applicazione** campo con valore 'Aspose.Diagram' e**PDF Producer** campo con valore, ad esempio 'Aspose.Diagram 17.9'.

Si noti che non è possibile incaricare Aspose.Diagram for .NET API di modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Utilizzare il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) costruttore di classe per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Il file sorgente.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_1.png)|


To export VSD diagram to PDF:

1. Creare un'istanza della classe Diagram.
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

|**Il file di output PDF.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_2.png)|
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Dividi più pagine**
Aspose.Diagram for .NET allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Usa pagina salva richiamata**
In case you have multiple pages, Aspose.Diagram for .NET allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **Classe TestDiagramPageSavingCallback**
{{< highlight "java" >}}

 classe pubblica TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{  public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)  {  Console.WriteLine("Inizia a salvare diagram pagina {0} di pagine {1}", args.PageIndex + 1, args.PageCountd_x00PageCountd);_x000PageCountd);   }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.WriteLine("Termina salvataggio diagram pagina {0} di pagine {1}", args.PageIndex + 1,PageCount args.Page);   //non restituisce le pagine dopo l'indice di pagina 8.  if (args.PageIndex >= 8)  {  args.HasMorePages = false;  } _x0_x0d_0}
