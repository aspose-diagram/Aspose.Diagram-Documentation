---
title:  Convertir Visio en d'autres formats
linktitle:  Convertir Visio en d'autres formats
type: docs
weight: 40
url: /fr/net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Exporter vers XML**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}


 Cet article explique comment exporter un Microsoft Visio diagram vers XML en utilisant[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX définit un XML diagram.
- VTX définit un modèle XML.
- VSX définit un gabarit XML.

 La[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Les constructeurs de la classe lisent un diagram et la méthode Save est utilisée pour enregistrer ou exporter un diagram dans un format de fichier différent. Les extraits de code de cet article montrent comment utiliser la méthode Save pour enregistrer un fichier Visio dans[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/) et[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
            
/* 1. Exporting VSDX to VDX */
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

// Save input VSD as VDX
diagram.Save(dataDir + "ExportToXML_out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
            
// Save input VSD as VSX
diagram.Save(dataDir + "ExportToXML_out.vsx", SaveFileFormat.VSX);
            
/* 3. Export VSD to VTX */
// Save input VSD as VTX
diagram.Save(dataDir + "ExportToXML_out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}


## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.
 Utilisez le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Le document source.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. Créez une instance de la classe Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Open a VSD file
Diagram diagram = new Diagram(dataDir + "LayOutShapesInCompactTreeStyle.vdx");

// Save diagram to an XPS format
diagram.Save(dataDir + "ExportToXPS_out.xps", SaveFileFormat.XPS);

{{< /highlight >}}


## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Utilisez le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

To export VSD diagram to SVG, perform the following steps:

1. Créez une instance de la classe Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save SVG Output file
diagram.Save(dataDir + "Output.svg", SaveFileFormat.SVG);

{{< /highlight >}}

## **Export to SWF**
This article explains how to export a Microsoft Visio diagram to SWF using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Utilisez le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' constructors to read the diagram files and then the Diagram class' Save method to export the diagram to SWF format. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**Entrez diagram.**|
|:- |
|![tâche : image_autre_texte](how-to-convert-a-visio-diagram_7.png)|

Après le code, il y a une image de la sortie.

To export VSD diagram to SWF::

- Créez une instance de la classe Diagram.
- Call the Diagram class' Save method and provide SWF format to export your diagram to SWF.
### **Exemple de programmation de visionneuse intégrée**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}

### **Sans exemple de programmation de visionneuse**
The SWF file created by these code snippets include an SWF viewer. Exclude the SWF viewer from the file using the following code.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Instantiate Diagram Object and open VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSWFWithoutViewer.vsd");

// Instantiate the Save Options
SWFSaveOptions options = new SWFSaveOptions();

// Set Save format as SWF
options.SaveFormat = SaveFileFormat.SWF;

// Exclude the embedded viewer
options.ViewerIncluded = false;

// Save the resultant SWF file
diagram.Save(dataDir + "ExportToSWFWithoutViewer_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}

## **Export a Diagram to XAML**
This article explains how to export a Microsoft Visio diagram to XAML (Extensible Application Markup Language) using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Utilisez le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' pour lire les fichiers diagram et la méthode Save pour exporter le diagram vers n'importe quel format d'image pris en charge.

Pour exporter un VSD diagram vers XAML :

1. Créez une instance de la classe Diagram.
1. Call the class' Save method and set XAML as the export format.
### **Export Microsoft Visio Drawing to XAML**
The code sample show how to export a diagram to XAML using C#.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");
// Save diagram
diagram.Save(dataDir + "ExportToXAML_out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}

## **Convertir le dessin Visio avec des formes sélectives**
À l'aide de Aspose.Diagram API, les développeurs peuvent sélectionner un groupe de formes pour convertir un dessin Visio dans tout autre format pris en charge. La classe RenderingSaveOptions propose un membre Shapes pour maintenir le groupe de formes. Chaque classe d'options de sauvegarde est la forme étendue de la classe RenderingSaveOptions.

Pour exporter un dessin Visio avec des formes sélectives :

1. Créez une instance de la classe Diagram.
1. Créez une instance de n'importe quelle classe SaveOption pour spécifier les paramètres comme indiqué ici :[Spécifiez les options d'enregistrement Visio](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. Appelez la méthode Save de l'objet de classe Diagram et passez l'objet de classe d'option de sauvegarde en tant que paramètre.
### **Convertir Visio Dessin avec exemple de programmation de formes sélectives**
L'exemple de code montre comment exporter un dessin avec des formes Visio sélectives.


{{< highlight csharp >}}
// the path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.Add(diagram.Pages[0].Shapes.GetShape(1));
shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing
diagram.Save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
