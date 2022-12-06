---
title:  Convertir Visio au format PDF
linktitle: Convertir Visio en PDF
type: docs
weight: 10
url: /fr/python-net/convert-visio-to-pdf/
description: Cette rubrique vous montre comment Aspose.Diagram permet de convertir Visio en formats PDF. Convertissez VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM en PDF avec quelques lignes de code.
---
## **Exporter au format PDF**
{{% alert color="primary" %}}

Aspose.Diagram pour Python via .NET écrit directement les informations sur le API et le numéro de version dans les documents de sortie. Par exemple, lors du rendu d'un dessin au format PDF, Aspose.Diagram for .NET remplit**Application** champ avec la valeur 'Aspose.Diagram' et**Producteur PDF** champ avec valeur, par exemple 'Aspose.Diagram 17.9'.

Veuillez noter que vous ne pouvez pas demander au Aspose.Diagram for .NET API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}}

 Cet article explique comment exporter un Microsoft Visio diagram au format PDF en utilisant[Aspose.Diagram pour Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilisez le constructeur de classe [Diagram] pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

L'image ci-dessous montre le VSD diagram que les extraits de code ci-dessous exportent au format PDF. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSM, VDX, VST, VSTX, VDX, VTX ou VSX).

|**Le fichier sources.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_1.png)|


Pour exporter VSD diagram au format PDF :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save des classes Diagram et définissez le format de sortie sur PDF.

Vous trouverez ci-dessous une image du fichier PDF de sortie.

|**Le fichier PDF de sortie.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_2.png)|
### **Exporter Microsoft Visio Dessin au format PDF**
Les exemples de code montrent comment exporter Microsoft Visio Dessin au format PDF à l'aide de Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
