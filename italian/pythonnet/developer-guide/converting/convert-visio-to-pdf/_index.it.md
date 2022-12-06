---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /it/python-net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Python via .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Applicazione** campo con valore 'Aspose.Diagram' e**PDF Producer** campo con valore, ad esempio 'Aspose.Diagram 17.9'.

Si noti che non è possibile incaricare Aspose.Diagram for .NET API di modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilizzare il costruttore di classe [Diagram] per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

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
The code samples show how to export Microsoft Visio Drawing to PDF using Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
