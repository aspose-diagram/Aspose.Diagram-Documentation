---
title: Convert Visio to HTML format 
linktitle: Convert Visio to HTML
type: docs
weight: 30
url: /fr/java/convert-visio-to-html/
description: This topic show you how to Aspose.Diagram allows to convert Visio to html formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to html with a few lines of code.
---
## **Exporter Visio vers HTML** **Exporter Visio vers HTML**
This article explains how to export a Microsoft Visio diagram to HTML using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format. Developers can save resultant HTML in the local storage or directly to a stream instance.

1. [Save resultant HTML in the local storage](/diagram/fr/java/how-to-convert-a-visio-diagram/).
1. [Save resultant HTML in a stream instance](/diagram/fr/java/how-to-convert-a-visio-diagram/).

The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

**Entrez diagram.**

![tâche : image_autre_texte](http://i.imgur.com/YX4BNNq.png)

In order to export VSD diagram to HTML, perform the following steps:

1. Créez une instance de la classe Diagram.
1. Call the Dagram class' Save method and set HTML as the output format.

L'image ci-dessous montre le fichier de sortie HTML.

**Output HTML diagram.**

![tâche : image_autre_texte](http://i.imgur.com/syavUqI.png)
### **Save resultant HTML in the local storage**
Le fichier résultant peut être enregistré en transmettant une chaîne de chemin complète, y compris le nom de fichier et l'extension, par exemple @"c:\temp\MyOutput.html".
#### **Save Resultant HTML in Local Storage Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Save resultant HTML in a stream instance**
It is for use case to save the resultant HTML in a database or repository without storing it in the local storage. This feature also embeds other resultant resources of the HTML, e.g. fonts, CSS (containing the style information) and images. Since it saves a single HTML file into the stream instance.
#### **Save Resultant HTML in a Stream Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
