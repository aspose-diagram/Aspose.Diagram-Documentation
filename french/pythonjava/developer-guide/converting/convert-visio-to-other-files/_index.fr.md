---
title:  Convertir Visio en d'autres formats
linktitle:  Convertir Visio en d'autres formats
type: docs
weight: 40
url: /fr/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML ,XAML avec quelques lignes de code.
---
**[A Microsoft Visio diagram à exporter.](ExportToXML.vsd)**

## **Exportation vers XML**
Cet article explique comment exporter un Microsoft Visio diagram vers XML en utilisant Aspose.Diagram pour Python via Java.

- VDX définit un XML diagram.
- VTX définit un modèle XML.
- VSX définit un gabarit XML.

Les constructeurs de la classe Diagram lisent un diagram et la méthode Save est utilisée pour enregistrer ou exporter un diagram dans un format de fichier différent. Les extraits de code de cet article montrent comment utiliser la méthode Save pour enregistrer un fichier Visio aux formats VDX, VTX et VSX.

### **Exportation VSD vers VDX**
VDX est un format de fichier XML basé sur un schéma qui vous permet d'enregistrer des diagrammes dans un format lisible par des produits autres que Microsoft Visio. C'est un format utile pour transférer des diagrammes entre des applications logicielles et conserver des données modifiables.

Pour exporter un VSD diagram vers VDX :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VDX.

### **Exportation de VSD à VSX**
VSX est un format XML permettant de définir des gabarits, les objets de base à partir desquels un diagram est construit. Lorsqu'un fichier Visio est converti en VSX, seuls les gabarits sont exportés.

Pour exporter un VSD diagram vers VSX :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VSX.

L'image ci-dessous montre le fichier de sortie VSX. Notez que les gabarits utilisés dans le diagram, et non le diagram lui-même, sont exportés.

### **Exporter VSD vers VTX**
TVX est une représentation XML d'un fichier modèle et stocke les paramètres du document.

Pour exporter un VSD diagram vers VTX :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe diagram pour écrire le fichier de dessin Visio au format VTX.

L'image ci-dessous montre le fichier de sortie VTX.

### **Exportation vers un exemple de programmation XML**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXML.py" >}}

## **Exportation vers XPS**
Cet article explique comment exporter un Microsoft Visio diagram vers XPS en utilisant Aspose.Diagram pour Python via Java.
Utilisez le constructeur de la classe Diagram pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Les extraits de code de cet article prennent le diagram ci-dessous comme entrée. Vous pouvez également utiliser d'autres formats diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX ou VSX).

Pour exporter VSD diagram vers XPS :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe Diagram et définissez XPS comme format de sortie.

L'image ci-dessous montre le fichier XPS de sortie.

### **Exportation vers un exemple de programmation XPS**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **Exporter un Diagram vers SVG**
Cet article explique comment exporter un Microsoft Visio diagram vers SVG (Scalable Vector Graphics) en utilisant Aspose.Diagram pour Python via Java.

Utilisez le constructeur de la classe Diagram pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Pour exporter VSD diagram vers SVG, procédez comme suit :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe et définissez SVG comme format d'exportation.

### **Exportation de Diagram vers un exemple de programmation SVG**
Les exemples de code montrent comment exporter un diagram vers SVG en utilisant Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **Exporter un Diagram vers XAML**
Cet article explique comment exporter un Microsoft Visio diagram vers XAML (Extensible Application Markup Language) en utilisant Aspose.Diagram pour Python via Java.

Utilisez le constructeur de la classe Diagram pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Pour exporter un VSD diagram vers XAML :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe et définissez XAML comme format d'exportation.

### **Exportation vers un exemple de programmation XAML**
L'exemple de code montre comment exporter un diagram vers XAML à l'aide de Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXAML.py" >}}

## **Convertir le dessin Visio avec des formes sélectives**
À l'aide de Aspose.Diagram API, les développeurs peuvent sélectionner un groupe de formes pour convertir un dessin Visio dans tout autre format pris en charge. La classe RenderingSaveOptions propose un membre Shapes pour maintenir le groupe de formes. Chaque classe d'options de sauvegarde est la forme étendue de la classe RenderingSaveOptions.

Pour exporter un dessin Visio avec des formes sélectives :

1. Créez une instance de la classe Diagram.
1. Créez une instance de n'importe quelle classe SaveOption pour spécifier les paramètres tels qu'ils sont racontés
1. Appelez la méthode de sauvegarde de l'objet de classe Diagram et passez l'objet de classe d'option de sauvegarde en tant que paramètre.

### **Convertir Visio Dessin avec exemple de programmation de formes sélectives**
L'exemple de code montre comment exporter un dessin avec des formes Visio sélectives.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ConvertVisioWithSelectiveShapes.py" >}}