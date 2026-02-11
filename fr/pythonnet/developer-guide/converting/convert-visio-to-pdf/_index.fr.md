---
title: Convert Visio to PDF format 
linktitle: Convert Visio to PDF
type: docs
weight: 10
url: /fr/python-net/convert-visio-to-pdf/
description: This topic show you how to Aspose.Diagram allows to convert Visio to PDF formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PDF with a few lines of code.
---
## **Export to PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Python via .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.Diagram for .NET populates **Application** champ avec la valeur 'Aspose.Diagram' et**PDF Producer** champ avec valeur, par exemple 'Aspose.Diagram 17.9'.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram for .NET API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to PDF using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilisez le constructeur de classe [Diagram] pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

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
The code samples show how to export Microsoft Visio Drawing to PDF using Python.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}

