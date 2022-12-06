---
title: Aspose.Diagram pour les exemples Node.js
type: docs
weight: 10
url: /fr/java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API vous permet de travailler avec des diagrammes Visio sans aucune compréhension du format de fichier sous-jacent. Vous pouvez créer des fichiers Visio VSDX à partir de zéro et convertir des fichiers VSDX en PNG avec seulement quelques lignes de code.
---
Aspose.Diagram pour Node.js est facile à utiliser et vous permet de travailler avec des diagrammes Visio sans aucune compréhension du format de fichier sous-jacent. Vous pouvez créer des fichiers Visio VSDX à partir de zéro en utilisant de simples lignes de code. Vous pouvez également convertir des fichiers VSDX en PNG avec seulement quelques lignes de code. Dans cet article, nous listons quelques exemples de base pour travailler avec les fichiers Visio VSDX en utilisant Aspose.Diagram pour Node.js API.
## **Créer Visio VSDX à partir de zéro en utilisant Node.js**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Exporter la page du fichier Visio VSDX au format PNG**
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
