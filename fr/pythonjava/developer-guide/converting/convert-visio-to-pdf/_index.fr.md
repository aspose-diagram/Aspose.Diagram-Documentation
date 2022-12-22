---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /fr/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Exporting to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Python via Java directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for Java populates **Application**champ avec la valeur 'Aspose.Diagram' et**PDF Producer**champ avec une valeur, par exemple 'Aspose.Diagram 17.9'.

Please note that you cannot instruct Aspose.Diagram for Python via Java to change or remove this information from output Documents.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using Aspose.Diagram for Python via Java.

Utilisez le constructeur de la classe Diagram pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

[Le VSD diagram](ExportToPDF.vsd) is the example drawing file to export PDF. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

To export VSD diagram to PDF:

1. Créez une instance de la classe Diagram.
1. Call the Diagram classs Save method and set the output format to PDF.

### **Exporting to PDF Programming Sample**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Fractionner plusieurs pages**
Aspose.Diagram for Java allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
