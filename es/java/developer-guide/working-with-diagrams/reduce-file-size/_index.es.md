---
title: Reducir tamaño de archivo
type: docs
weight: 50
url: /es/java/reduce-file-size/
description: Esta sección explica cómo reducir el tamaño del archivo de diagram a Aspose.Diagram.
---
## **Reducir tamaño de archivo**
 Aspose.Diagram for Java API permite a los desarrolladores eliminar información oculta de un diagram para reducir el tamaño del archivo.
 los[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) El objeto representa el área de dibujo de una página de primer plano o una página de fondo. Para reducir el tamaño del archivo, puede usar[Quitar elemento de información oculta](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) propiedades en**Eliminar información oculta ()** método de[Diagram](https://reference.aspose.com/diagram/java)clase. El siguiente ejemplo de código muestra cómo eliminar la información oculta de diagram.

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
