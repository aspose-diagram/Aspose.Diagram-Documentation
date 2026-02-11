---
title:  Convertir Visio en d'autres formats
linktitle:  Convertir Visio en d'autres formats
type: docs
weight: 40
url: /fr/java/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Exportation vers XML**
 Cet article explique comment exporter un Microsoft Visio diagram vers XML en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- VDX définit un XML diagram.
- VTX définit un modèle XML.
- VSX définit un gabarit XML.

 La[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) Les constructeurs de la classe lisent un diagram et la méthode Save est utilisée pour enregistrer ou exporter un diagram dans un format de fichier différent. Les extraits de code de cet article montrent comment utiliser la méthode Save pour enregistrer un fichier Visio dans[VDX](/diagram/fr/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/fr/java/how-to-convert-a-visio-diagram/) et[VSX](/diagram/fr/java/how-to-convert-a-visio-diagram/).

L'image ci-dessous montre le diagram qui est exporté dans les extraits de code ci-dessous. Le fichier exporté est affiché avant chaque extrait de code.

**Un Microsoft Visio diagram sur le point d'être exporté.**

![tâche : image_autre_texte](http://i.imgur.com/XWajazh.png)
### **Exportation VSD vers VDX**
VDX est un format de fichier XML basé sur un schéma qui vous permet d'enregistrer des diagrammes dans un format lisible par des produits autres que Microsoft Visio. C'est un format utile pour transférer des diagrammes entre des applications logicielles et conserver des données modifiables.

Pour exporter un VSD diagram vers VDX :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VDX.

**Le fichier VDX exporté.**

![tâche : image_autre_texte](http://i.imgur.com/OJ1jpgh.png)
### **Exportation de VSD à VSX**
VSX est un format XML permettant de définir des gabarits, les objets de base à partir desquels un diagram est construit. Lorsqu'un fichier Visio est converti en VSX, seuls les gabarits sont exportés.

Pour exporter un VSD diagram vers VSX :

- Créez une instance de la classe Diagram.
- Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VSX.

L'image ci-dessous montre le fichier de sortie VSX. Notez que les gabarits utilisés dans le diagram, et non le diagram lui-même, sont exportés.

**Le fichier VSX exporté.**

![tâche : image_autre_texte](http://i.imgur.com/gkZrxCN.png)
### **Exporter VSD vers VTX**
TVX est une représentation XML d'un fichier modèle et stocke les paramètres du document.

Pour exporter un VSD diagram vers VTX :

1. Créez une instance de la classe Diagram.
1. Appelez la méthode Save de la classe diagram pour écrire le fichier de dessin Visio au format VTX.

L'image ci-dessous montre le fichier de sortie VTX.

**Le fichier de sortie VTX.**

![tâche : image_autre_texte](http://i.imgur.com/E6pUvGD.jpg)
### **Exportation vers un exemple de programmation XML**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXML.class);

/* 1. Exporting VSDX to VDX */
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

//Save input VSD as VDX
diagram.save(dataDir + "ExportToXML_Out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
        
//Save input VSD as VSX
diagram.save(dataDir + "ExportToXML_Out.vsx", SaveFileFormat.VSX);
        
/* 3. Export VSD to VTX */
//Save input VSD as VTX
diagram.save(dataDir + "ExportToXML_Out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}

## **Exporting to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**Le document source.**

![tâche : image_autre_texte](http://i.imgur.com/P3gaA34.png)

To export VSD diagram to XPS:

1. Créez une instance de la classe Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.

L'image ci-dessous montre le fichier de sortie XPS.

**The output XPS.**

![tâche : image_autre_texte](http://i.imgur.com/1ESRxSy.png)
### **Exporting to XPS Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXPS.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir+ "ExportToXPS.vsd");

// Save as XPS
diagram.save(dataDir + "ExportToXPS_Out.xps", SaveFileFormat.XPS);

{{< /highlight >}}

## **Exporting a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

To export VSD diagram to SVG, perform the following steps:

1. Créez une instance de la classe Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Exporting Diagram to SVG Programming Sample**
The code samples show how to export a diagram to SVG using Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToSVG.class);

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save as SVG
diagram.save(dataDir+ "ExportToSVG_Out.svg", SaveFileFormat.SVG);

{{< /highlight >}}

## **Exporting a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilisez le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Pour exporter un VSD diagram vers XAML :

1. Créez une instance de la classe Diagram.
1. Call the class' Save method and set XAML as the export format.
### **Exporting to XAML Programming Sample**
The code sample show how to export a diagram to XAML using Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXAML.class); 

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");

// save as XAML
diagram.save(dataDir + "ExportToXAML_Out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}


## **Convertir le dessin Visio avec des formes sélectives**
À l'aide de Aspose.Diagram API, les développeurs peuvent sélectionner un groupe de formes pour convertir un dessin Visio dans tout autre format pris en charge. La classe RenderingSaveOptions propose un membre Shapes pour maintenir le groupe de formes. Chaque classe d'options de sauvegarde est la forme étendue de la classe RenderingSaveOptions.

Pour exporter un dessin Visio avec des formes sélectives :

1. Créez une instance de la classe Diagram.
1. Créez une instance de n'importe quelle classe SaveOption pour spécifier les paramètres comme indiqué ici :[Spécifiez les options d'enregistrement Visio](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. Appelez la méthode de sauvegarde de l'objet de classe Diagram et passez l'objet de classe d'option de sauvegarde en tant que paramètre.
### **Convertir Visio Dessin avec exemple de programmation de formes sélectives**
L'exemple de code montre comment exporter un dessin avec des formes Visio sélectives.


{{< highlight java >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";
		
// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.getPages().get(0).getShapes().getShape(1));
shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing
diagram.save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
