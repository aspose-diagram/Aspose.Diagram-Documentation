---
title: Aspose.Diagram för Node.js-exempel
type: docs
weight: 10
url: /sv/java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API låter dig arbeta med Visio diagram utan någon förståelse för underliggande filformat. Du kan skapa Visio VSDX-filer från början och konvertera VSDX-filer till PNG med bara ett par rader kod.
---
Aspose.Diagram för Node.js är lätt att använda och låter dig arbeta med Visio-diagram utan någon förståelse för underliggande filformat. Du kan skapa Visio VSDX filer från början med enkla kodrader. Du kan också konvertera VSDX-filer till PNG med bara ett par rader kod. I den här artikeln listar vi några grundläggande exempel för att arbeta med Visio VSDX-filer med Aspose.Diagram för Node.js API.
## **Skapa Visio VSDX från Scratch med Node.js**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Exportera sida av Visio VSDX fil till PNG Format**
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
