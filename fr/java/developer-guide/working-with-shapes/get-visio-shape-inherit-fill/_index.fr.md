---
title: Obtenir Visio Shape Inherit Fill
type: docs
weight: 100
url: /fr/java/get-visio-shape-inherit-fill/
description: Cette section explique comment obtenir le style de remplissage de la forme visio hérité de son style parent et maître avec Aspose.Diagram.
---
### **Récupérer les données de remplissage héritées d'une forme Visio**
Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir les données de remplissage héritées d'une forme Visio. La propriété InheritFill, exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) classe, contient les valeurs de formatage de remplissage pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de remplissage héritées**
L'extrait de code suivant récupère les données de remplissage héritées de la forme. Veuillez vérifier cet exemple de code :


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}


