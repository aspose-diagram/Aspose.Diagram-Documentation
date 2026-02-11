---
title: Fusionner Combiner Diagram
type: docs
weight: 30
url: /fr/java/merge-combine-diagram/
description: Cette section explique comment combiner le fichier visio
---
## **Scénarios d'utilisation possibles**

 Aspose.Diagram vous permet de combiner deux fichiers visio en un seul.
 Aspose.Diagram for Java API a le[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) classe qui représente un dessin Visio.
En utilisant la méthode[**Combiner**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) dans[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) classe pour combiner des diagrammes.

## **Exemple de code**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CombineDiagram.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(dataDir + Drawing2.vsdx");

diagram2.combine(diagram);

// save in the VSDX format
diagram.save(dataDir + "CombineDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

