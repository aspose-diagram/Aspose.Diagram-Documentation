---
title:  Convertir Visio en d'autres formats
linktitle:  Convertir Visio en d'autres formats
type: docs
weight: 40
url: /fr/python-net/convert-visio-to-other-files/
description: Cette rubrique vous montre comment Aspose.Diagram permet de convertir Visio aux formats SVG, XPS, XML, XAML. Convertissez VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM en SVG, XPS, XML, XAML avec quelques lignes de code.
---
## **Exporter vers XML**
### **Exporter Microsoft Visio Dessin au format PDF**
Les exemples de code montrent comment exporter Microsoft Visio Dessin au format PDF à l'aide de C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}

 Cet article explique comment exporter un Microsoft Visio diagram vers XML en utilisant[Aspose.Diagram pour Python via .NET](https://products.aspose.com/diagram/python-net/) API.

- VDX définit un XML diagram.
- VTX définit un modèle XML.
- VSX définit un gabarit XML.

 Les constructeurs de la classe [Diagram] lisent un diagram et la méthode Save est utilisée pour enregistrer ou exporter un diagram dans un format de fichier différent. Les extraits de code de cet article montrent comment utiliser la méthode Save pour enregistrer un fichier Visio dans[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/) et[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

L'image ci-dessous montre le diagram qui est exporté dans les extraits de code ci-dessous. Le fichier exporté est affiché avant chaque extrait de code.

|**Un Microsoft Visio diagram sur le point d'être exporté.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_3.png)|

### **Exporter VSD vers VDX**
VDX est un format de fichier XML basé sur un schéma qui vous permet d'enregistrer des diagrammes dans un format lisible par des produits autres que Microsoft Visio. C'est un format utile pour transférer des diagrammes entre des applications logicielles et conserver des données modifiables.

Pour exporter un VSD diagram vers VDX :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VDX.

|**Le fichier VDX exporté.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_4.png)|

### **Exporter de VSD à VSX**
VSX est un format XML permettant de définir des gabarits, les objets de base à partir desquels un diagram est construit. Lorsqu'un fichier Visio est converti en VSX, seuls les gabarits sont exportés.

Pour exporter un VSD diagram vers VSX :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VSX.
### **Exporter VSD vers VTX**
TVX est une représentation XML d'un fichier modèle et stocke les paramètres du document.

Pour exporter un VSD diagram vers VTX :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe diagram pour écrire le fichier de dessin Visio au format VTX.
### **Exporter Microsoft Visio Dessin vers XML**
Les exemples de code montrent comment exporter le dessin Microsoft Visio vers XML à l'aide de C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXml.py" >}}

## **Exporter vers XPS**
 Cet article explique comment exporter un Microsoft Visio diagram vers XPS en utilisant[Aspose.Diagram pour Python via .NET](https://products.aspose.com/diagram/python-net/) API.
Utilisez le constructeur de la classe [Diagram] pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Les extraits de code de cet article prennent le diagram ci-dessous comme entrée. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX ou VSX).

|**Le document source.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_5.png)|


Pour exporter VSD diagram vers XPS :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe Diagram et définissez XPS comme format de sortie.
### **Exporter Microsoft Visio Dessin vers XPS**
Les exemples de code montrent comment exporter le dessin Microsoft Visio vers XPS à l'aide de C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXps.py" >}}

## **Exporter un Diagram vers SVG**
Cet article explique comment exporter un Microsoft Visio diagram vers SVG (Scalable Vector Graphics) en utilisant[Aspose.Diagram pour Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilisez le constructeur de la classe [Diagram] pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Pour exporter VSD diagram vers SVG, procédez comme suit :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe et définissez SVG comme format d'exportation.
### **Exporter Microsoft Visio Dessin vers SVG**
Les exemples de code montrent comment exporter un diagram vers SVG en utilisant C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToSvg.py" >}}

Pour exporter un dessin Visio avec des formes sélectives :

1. Créez une instance de la classe Diagram.
1. Créez une instance de n'importe quelle classe SaveOption pour spécifier les paramètres comme indiqué ici :[Spécifiez les options d'enregistrement Visio](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Appelez la méthode Save de l'objet de classe Diagram et passez l'objet de classe d'option de sauvegarde en tant que paramètre.
### **Convertir Visio Dessin avec exemple de programmation de formes sélectives**
L'exemple de code montre comment exporter un dessin avec des formes Visio sélectives.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-PythonNet-ConvertVisioWithSelectiveShapes.py" >}}