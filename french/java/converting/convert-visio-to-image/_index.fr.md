---
title:  Convertir Visio en formats Images
linktitle: Convertir Visio en Images
type: docs
weight: 20
url: /fr/java/convert-visio-to-image/
description: Cette rubrique vous montre comment Aspose.Diagram permet de convertir Visio en différents formats d'images. Convertissez Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM en images PNG, JPEG, BMP avec quelques lignes de code.
---
## **Exportation de diagrammes vers des formats de fichier image**
 Cet article explique comment exporter un Microsoft Visio diagram vers une image en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge. L'image ci-dessous montre un fichier VSD sur le point d'être enregistré au format PNG. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX ou VSX).
**Le fichier sources. Notez que les étiquettes Flèche et Triangle sont en gras.**

![tâche : image_autre_texte](http://i.imgur.com/WOV36ek.png)

Pour exporter un diagram vers une image :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram et définissez le format d'image vers lequel vous souhaitez exporter. Le fichier image de sortie ressemble au fichier d'origine.

**Le fichier PNG de sortie.**

![tâche : image_autre_texte](http://i.imgur.com/WOV36ek.png)
### **Exemple de programmation d'exportation vers un fichier image**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

Il est également possible d'enregistrer une page particulière dans l'image, au lieu du document entier :

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}