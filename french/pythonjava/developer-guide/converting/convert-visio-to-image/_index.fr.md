---
title:  Convertir Visio en formats Images
linktitle: Convertir Visio en Images
type: docs
weight: 20
url: /fr/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a quelques lignes de code.
---
## **Exportation de diagrammes vers des formats de fichier image**
Cet article explique comment exporter un Microsoft Visio diagram vers une image en utilisant Aspose.Diagram pour Python via Java.

Utilisez le constructeur de la classe Diagram pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge. L'image ci-dessous montre un fichier VSD sur le point d'être enregistré au format PNG. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX ou VSX).

**[L'exemple de fichier VSD.](ExportToImage.vsd)**

Pour exporter un diagram vers une image :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram et définissez le format d'image vers lequel vous souhaitez exporter. Le fichier image de sortie ressemble au fichier d'origine.

**Le fichier PNG de sortie.**

![tâche : image_autre_texte](ExportToImage.png)
### **Exemple de programmation d'exportation vers un fichier image**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

Il est également possible d'enregistrer une page particulière dans l'image, au lieu du document entier :

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}