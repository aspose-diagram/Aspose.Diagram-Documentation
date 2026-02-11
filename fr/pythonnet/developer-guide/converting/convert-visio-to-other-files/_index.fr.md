---
title:  Convertir Visio en d'autres formats
linktitle:  Convertir Visio en d'autres formats
type: docs
weight: 40
url: /fr/python-net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Exporter vers XML**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}


 Cet article explique comment exporter un Microsoft Visio diagram vers XML en utilisant[Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

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


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the vdx format
diagram.save("Visio_out.vdx", SaveFileFormat.VDX)

#// Save diagram in the vtx format
diagram.save("Visio_out.vtx", SaveFileFormat.VTX)

#// Save diagram in the vsx format
diagram.save("Visio_out.vsx", SaveFileFormat.VSX)
{{< /highlight >}}


## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.
Utilisez le constructeur de la classe [Diagram] pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Le document source.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. Créez une instance de la classe Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the xps format
diagram.save("Visio_out.xps", SaveFileFormat.XPS)
{{< /highlight >}}


## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilisez le constructeur de la classe [Diagram] pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

To export VSD diagram to SVG, perform the following steps:

1. Créez une instance de la classe Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the svg format
diagram.save("Visio_out.svg", SaveFileFormat.SVG)
{{< /highlight >}}


Pour exporter un dessin Visio avec des formes sélectives :

1. Créez une instance de la classe Diagram.
1. Créez une instance de n'importe quelle classe SaveOption pour spécifier les paramètres comme indiqué ici :[Spécifiez les options d'enregistrement Visio](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Appelez la méthode Save de l'objet de classe Diagram et passez l'objet de classe d'option de sauvegarde en tant que paramètre.
### **Convertir Visio Dessin avec exemple de programmation de formes sélectives**
L'exemple de code montre comment exporter un dessin avec des formes Visio sélectives.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.SVGSaveOptions()
shapes = options.shapes;
#// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.pages[0].shapes.get_shape(1));
shapes.add(diagram.pages[0].shapes.get_shape(2));
    
#// Save one page only, by page index
options.page_index = 0
    
#// Save resultant svg file
diagram.save("ExportToSvg_out.svg", options)
{{< /highlight >}}
