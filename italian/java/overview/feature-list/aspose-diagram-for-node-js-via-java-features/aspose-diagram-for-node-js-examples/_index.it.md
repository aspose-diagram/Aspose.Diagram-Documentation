---
title: Aspose.Diagram per Node.js Esempi
type: docs
weight: 10
url: /it/java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API ti consente di lavorare con i diagrammi Visio senza alcuna comprensione del formato di file sottostante. Puoi creare file Visio VSDX da zero e convertire i file VSDX in PNG con solo un paio di righe di codice.
---
Aspose.Diagram per Node.js è facile da usare e ti consente di lavorare con i diagrammi Visio senza alcuna comprensione del formato di file sottostante. Puoi creare file Visio VSDX da zero utilizzando semplici righe di codice. Puoi anche convertire i file VSDX in PNG con solo un paio di righe di codice. In questo articolo, elenchiamo alcuni esempi di base per lavorare con i file Visio VSDX utilizzando Aspose.Diagram per Node.js API.
## **Crea Visio VSDX da zero usando Node.js**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Esporta la pagina del file Visio VSDX in formato PNG**
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
