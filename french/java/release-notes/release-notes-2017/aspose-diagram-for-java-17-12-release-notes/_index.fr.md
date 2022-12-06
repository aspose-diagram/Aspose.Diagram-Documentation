---
title: Aspose.Diagram for Java 17.12 Notes de mise à jour
type: docs
weight: 10
url: /fr/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|Fournissez le seul API pour convertir une forme Visio en PDF|Renforcement|
|DIAGRAMJAVA-50291|Fournissez le seul API pour convertir une forme Visio en HTML|Renforcement|
|DIAGRAMJAVA-50572|La méthode Shape.connectedShapes ne récupère pas les nœuds sortants|Renforcement|
|DIAGRAMJAVA-50391|Les images inversées et les flèches sont générées lors de la conversion d'un VSD en SVG|Punaise|
|DIAGRAMJAVA-50570|VSD au format PDF - les éléments de texte supplémentaires sont ajoutés|Punaise|
|DIAGRAMJAVA-50571|Import VSDX - une erreur s'est produite dans l'élément de forme|Punaise|
|DIAGRAMJAVA-50573|VSD à SVG - les lignes d'une forme de groupe sont manquantes|Punaise|
|DIAGRAMJAVA-50575|VSD vers SVG - les éléments de texte sont manquants|Punaise|
|DIAGRAMJAVA-50576|La procédure d'importation VDX génère une erreur d'élément de page|Punaise|
### **Ajoute un membre Copy dans la classe Shape**
Le membre de copie prend une instance de forme cible, comme paramètre pour cloner cette forme.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **Ajoute un membre toPdf dans la classe Shape**
Le membre toPdf convertit une forme au format PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Ajoute le membre toHTML dans la classe Shape**
Le membre toHTML convertit une forme au format PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **Exemples d'utilisation**
Veuillez consulter la liste des rubriques d'aide ajoutées dans les documents Wiki Aspose.Diagram :

1. [Copier une forme Visio dans une autre instance de forme](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Convertir la forme Visio en PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [Convertir la forme Visio en HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


