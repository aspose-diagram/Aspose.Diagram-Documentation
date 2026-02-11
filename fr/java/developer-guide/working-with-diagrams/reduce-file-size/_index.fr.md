---
title: Réduire la taille du fichier
type: docs
weight: 50
url: /fr/java/reduce-file-size/
description: Cette section explique comment réduire la taille du fichier d'un diagram à Aspose.Diagram.
---
## **Réduire la taille du fichier**
 Aspose.Diagram for Java API permet aux développeurs de supprimer les informations cachées d'un diagram pour réduire la taille du fichier.
 La[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) L'objet représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. Afin de réduire la taille du fichier, vous pouvez utiliser[Supprimer l'élément d'information caché](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) propriétés dans**Supprimer les informations cachées ()** méthode de[Diagram](https://reference.aspose.com/diagram/java)classer. L'exemple de code ci-dessous montre comment supprimer les informations masquées de diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}
```
