---
title: Obtenir la ligne d'héritage de forme Visio
type: docs
weight: 100
url: /fr/java/get-visio-shape-inherit-line/
description: Cette section explique comment obtenir le style de ligne de la forme visio hérité de son style parent et le maîtriser avec Aspose.Diagram.
---
### **Récupérer les données de ligne héritées d'une forme Visio**
 Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir ou définir les données de ligne héritées d'une forme Visio. La propriété InheritLine, exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) classe, contient les valeurs de formatage de ligne pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de ligne héritées**
L'extrait de code suivant récupère les données de ligne héritées de la forme. Veuillez vérifier cet exemple de code :


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}


