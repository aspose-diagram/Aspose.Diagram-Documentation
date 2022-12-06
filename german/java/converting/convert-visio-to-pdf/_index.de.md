---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /de/java/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Exporting to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for Java populates **Anwendung**Feld mit dem Wert 'Aspose.Diagram' und**PDF Producer**Feld mit einem Wert, zB 'Aspose.Diagram 17.9'.

Bitte beachten Sie, dass Sie Aspose.Diagram for Java API nicht anweisen können, diese Informationen aus Ausgabedokumenten zu ändern oder zu entfernen.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Verwenden Sie die[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) -Klasse'-Konstruktor, um die diagram-Dateien zu lesen, und die Save-Methode, um diagram in ein beliebiges unterstütztes Bildformat zu exportieren.

The image below shows the VSD diagram that the code snippets below export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Die Quelldatei.**

![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_1.png)

To export VSD diagram to PDF:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Call the Diagram classs Save method and set the output format to PDF.

Below is an image of the output PDF file.

**Die Ausgabedatei PDF.**

![todo: Bild_alt_Text](how-to-convert-a-visio-diagram_2.png)
### **Exporting to PDF Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Mehrere Seiten aufteilen**
Aspose.Diagram for Java allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Verwenden Sie den Seitenspeicher-Callback**
In case you have multiple pages, Aspose.Diagram for Java allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **TestDiagramPageSavingCallback-Klasse**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
