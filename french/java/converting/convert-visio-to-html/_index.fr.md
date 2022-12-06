---
title:  Convertir Visio au format HTML
linktitle: Convertir Visio en HTML
type: docs
weight: 30
url: /fr/java/convert-visio-to-html/
description: Cette rubrique vous montre comment Aspose.Diagram permet de convertir Visio en formats html. Convertissez VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM en html avec quelques lignes de code.
---
## **Exporter Visio au format HTML** **Exporter Visio au format HTML**
 Cet article explique comment exporter un Microsoft Visio diagram vers HTML en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) constructeur de classe pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge. Les développeurs peuvent enregistrer le code HTML résultant dans le stockage local ou directement dans une instance de flux.

1. [Enregistrer le HTML résultant dans le stockage local](/diagram/fr/java/how-to-convert-a-visio-diagram/).
1. [Enregistrer le HTML résultant dans une instance de flux](/diagram/fr/java/how-to-convert-a-visio-diagram/).

L'image ci-dessous montre un fichier VSD sur le point d'être enregistré au format PNG. Vous pouvez également utiliser d'autres formats diagram (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX ou 0761)1

**Entrez diagram.**

![tâche : image_autre_texte](http://i.imgur.com/YX4BNNq.png)

Pour exporter VSD diagram au format HTML, procédez comme suit :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe Dagram et définissez HTML comme format de sortie.

L'image ci-dessous montre le fichier HTML de sortie.

**Sortie HTML diagram.**

![tâche : image_autre_texte](http://i.imgur.com/syavUqI.png)
### **Enregistrer le HTML résultant dans le stockage local**
Le fichier résultant peut être enregistré en transmettant une chaîne de chemin complète, y compris le nom de fichier et l'extension, par exemple @"c:\temp\MyOutput.html".
#### **Enregistrer le HTML résultant dans l'exemple de programmation de stockage local**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Enregistrer le HTML résultant dans une instance de flux**
Il s'agit d'un cas d'utilisation pour enregistrer le code HTML résultant dans une base de données ou un référentiel sans le stocker dans le stockage local. Cette fonctionnalité intègre également d'autres ressources résultantes du HTML, par exemple les polices, le CSS (contenant les informations de style) et les images. Puisqu'il enregistre un seul fichier HTML dans l'instance de flux.
#### **Enregistrer le code HTML résultant dans un exemple de programmation de flux**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
