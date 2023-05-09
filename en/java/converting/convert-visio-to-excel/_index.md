---
title: Convert Visio to Excel format 
linktitle: Convert Visio to Excel
type: docs
weight: 10
url: /java/convert-visio-to-excel/
description: This topic show you how to Aspose.Diagram allows to convert Visio to Excel formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to Excel with a few lines of code.
---

## **Exporting to Excel**
{{% alert color="primary" %}}

Aspose.Diagram for Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to Excel, Aspose.Diagram for Java populates **Application** field with value 'Aspose.Diagram' and **Excel Producer** field with a value, e.g 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for Java API to change or remove this information from output Documents.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to Excel using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

Use the [Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.

The image below shows the VSD diagram that the code snippets below export Excel. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**The source file.**

To export VSD diagram to Excel:

1. Create an instance of the Diagram class.
1. Call the Diagram classs Save method and set the output format to Excel.

### **Exporting to Excel Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToCSV-ExportToCSV.java" >}}

