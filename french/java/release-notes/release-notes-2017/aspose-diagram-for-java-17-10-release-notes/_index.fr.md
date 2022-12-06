---
title: Aspose.Diagram for Java 17.10 Notes de mise à jour
type: docs
weight: 30
url: /fr/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JpegQuality n'a aucun effet sur le document de sortie|Renforcement|
|DIAGRAMJAVA-50548|Sortie VSDX - la ligne de connexion passant par la limite de la forme|Punaise|
|DIAGRAMJAVA-50550|La section Shape Transform ne conserve pas les formules|Punaise|
|DIAGRAMJAVA-50551|VSDX vers PNG - rendu incorrect des coins de la forme|Punaise|
|DIAGRAMJAVA-50552|Les couleurs de remplissage ne sont pas conservées lors de l'enregistrement d'un dessin Visio au format SVG|Punaise|
|DIAGRAMJAVA-50553|Rendu incorrect des lignes lors de l'enregistrement d'un dessin Visio au format SVG|Punaise|
|DIAGRAMJAVA-50554|Les couleurs de remplissage ne sont pas conservées lors de l'enregistrement d'un dessin Visio au format SVG|Punaise|
|DIAGRAMJAVA-50555|Rendu incorrect des lignes lors de l'enregistrement d'un dessin Visio au format SVG|Punaise|
|DIAGRAMJAVA-50559|VSDM à VDX - les lignes de connexion ne sont pas connectées aux formes|Punaise|
|DIAGRAMJAVA-50561|Le dessin VSDX est corrompu après l'ajout de l'élément SolutionXML|Punaise|
### **Ajoute SameAsPdfConversionArea dans ImageSaveOptions**
Il spécifie s'il faut enregistrer la zone de la même manière que PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
