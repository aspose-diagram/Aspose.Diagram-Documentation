---
title:  Convertir Visio en formats Images
linktitle: Convertir Visio en Images
type: docs
weight: 20
url: /fr/java/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportation de diagrammes vers des formats de fichier image**
 Cet article explique comment exporter un Microsoft Visio diagram vers une image en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.
**Le fichier sources. Notez que les étiquettes Flèche et Triangle sont en gras.**

![tâche : image_autre_texte](http://i.imgur.com/WOV36ek.png)

Pour exporter un diagram vers une image :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram et définissez le format d'image vers lequel vous souhaitez exporter. Le fichier image de sortie ressemble au fichier d'origine.

**Le fichier de sortie PNG.**

![tâche : image_autre_texte](http://i.imgur.com/WOV36ek.png)
### **Exemple de programmation d'exportation vers un fichier image**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

Il est également possible d'enregistrer une page particulière dans l'image, au lieu du document entier :

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}