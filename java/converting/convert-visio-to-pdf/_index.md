---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /java/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---

## **Exporting to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for Java populates **Application** field with value 'Aspose.Diagram' and **PDF Producer** field with a value, e.g 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for Java API to change or remove this information from output Documents.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

Use the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**The source file.**

![todo:image_alt_text](how-to-convert-a-visio-diagram_1.png)

To export VSD diagram to PDF:

1. Create an instance of the Diagram class.
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

**The output PDF file.**

![todo:image_alt_text](how-to-convert-a-visio-diagram_2.png)
### **Exporting to PDF Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
