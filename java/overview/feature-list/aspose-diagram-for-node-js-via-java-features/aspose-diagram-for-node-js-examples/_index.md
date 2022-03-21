---
title: Aspose.Diagram for Node.js Examples
type: docs
weight: 10
url: /java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API lets you work with Visio diagrams without any understanding of underlying file format. You can create Visio VSDX files from scratch and convert VSDX files to PNG with just a couple of lines of code.
---

Aspose.Diagram for Node.js is easy to use and lets you work with Visio diagrams without any understanding of underlying file format. You can create Visio VSDX files from scratch using simple lines of code. You can also convert VSDX files to PNG with just a couple of lines of code. In this article, we list some basic examples for working with Visio VSDX files using Aspose.Diagram for Node.js API.
## **Create Visio VSDX from Scratch using Node.js**
{{< highlight java >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Export Page of Visio VSDX File to PNG Format**
{{< highlight java >}}

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
