---
title:  Convertir Visio au format HTML
linktitle: Convertir Visio en HTML
type: docs
weight: 30
url: /fr/python-net/convert-visio-to-html/
description: Cette rubrique vous montre comment Aspose.Diagram permet de convertir Visio en formats html. Convertissez VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM en html avec quelques lignes de code.
---
## **Exporter Visio au format HTML**
 Cet article explique comment exporter un Microsoft Visio diagram vers HTML en utilisant[Aspose.Diagram pour Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilisez le constructeur de classe Diagram pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge. Les développeurs peuvent enregistrer le code HTML résultant dans le stockage local ou directement dans une instance de flux.

1. [Enregistrer le HTML résultant dans le stockage local](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Enregistrer le HTML résultant dans une instance de flux](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

L'image ci-dessous montre un fichier VSD sur le point d'être enregistré au format PNG. Vous pouvez également utiliser d'autres formats diagram (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX ou 0761)1

|**Entrez diagram.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_6.png)|
Pour exporter VSD diagram au format HTML, procédez comme suit :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe Dagram et définissez HTML comme format de sortie.
### **Enregistrer le HTML résultant dans le stockage local**
Le fichier résultant peut être enregistré en transmettant une chaîne de chemin complète, y compris le nom de fichier et l'extension, par exemple @"c:\temp\MyOutput.html".
#### **Enregistrer le HTML résultant dans l'exemple de programmation de stockage local**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToHTML.py" >}}
