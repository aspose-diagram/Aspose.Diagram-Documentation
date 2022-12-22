---
title:  Convertir Visio en formats Images
linktitle: Convertir Visio en Images
type: docs
weight: 20
url: /fr/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportation de diagrammes vers des formats de fichier image**
This article explains how to export a Microsoft Visio diagram to an image using Aspose.Diagram for Python via Java.

Use the Diagram class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**[L'exemple de fichier VSD.](ExportToImage.vsd)**

Pour exporter un diagram vers une image :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram et définissez le format d'image vers lequel vous souhaitez exporter. Le fichier image de sortie ressemble au fichier d'origine.

**Le fichier de sortie PNG.**

![tâche : image_autre_texte](ExportToImage.png)
### **Exemple de programmation d'exportation vers un fichier image**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

Il est également possible d'enregistrer une page particulière dans l'image, au lieu du document entier :

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}