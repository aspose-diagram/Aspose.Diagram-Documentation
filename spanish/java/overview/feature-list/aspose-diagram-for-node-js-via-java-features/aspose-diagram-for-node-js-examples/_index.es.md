---
title: Aspose.Diagram para ejemplos de Node.js
type: docs
weight: 10
url: /es/java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API le permite trabajar con diagramas Visio sin comprender el formato de archivo subyacente. Puede crear archivos Visio VSDX desde cero y convertir archivos VSDX a PNG con solo un par de líneas de código.
---
Aspose.Diagram para Node.js es fácil de usar y le permite trabajar con diagramas Visio sin comprender el formato de archivo subyacente. Puede crear archivos Visio VSDX desde cero usando simples líneas de código. También puede convertir archivos VSDX a PNG con solo un par de líneas de código. En este artículo, enumeramos algunos ejemplos básicos para trabajar con archivos Visio VSDX usando Aspose.Diagram para Node.js API.
## **Cree Visio VSDX desde cero usando Node.js**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Exportar página de archivo Visio VSDX a formato PNG**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

diagram = new aspose.diagram.Diagram("template.vsdx");

// Save diagram as PNG

options = new aspose.diagram.ImageSaveOptions(aspose.diagram.SaveFileFormat.PNG);

// Save one page only, by page index

options.setPageIndex(0);

// Save resultant Image file

diagram.save("output.png", options);

{{< /highlight >}}
