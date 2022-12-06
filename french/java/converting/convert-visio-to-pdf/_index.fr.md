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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Fractionner plusieurs pages**
Aspose.Diagram for Java allows splitting multiple pages while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Utiliser le rappel d'enregistrement de page**
In case you have multiple pages, Aspose.Diagram for Java allows using page saving callback while converting the Microsoft Visio Diagram to PDF. The following code snippet shows the functionality.  

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **Classe TestDiagramPageSavingCallbackTestDiagramPageSavingCallback Class**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
