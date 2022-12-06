---
title: Aspose.Diagram 用于 Node.js 示例
type: docs
weight: 10
url: /zh/java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API 让您可以在不了解底层文件格式的情况下使用 Visio 图表。您可以从头开始创建 Visio VSDX 文件，只需几行代码即可将 VSDX 文件转换为 PNG。
---
Node.js 的 Aspose.Diagram 易于使用，让您可以使用 Visio 图表，而无需了解底层文件格式。您可以使用简单的代码行从头开始创建 Visio VSDX 文件。您还可以使用几行代码将 VSDX 文件转换为 PNG。在本文中，我们列出了使用 Aspose.Diagram for Node.js API 处理 Visio VSDX 文件的一些基本示例。
## **使用 Node.js 从头开始创建 Visio VSDX**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **将Visio VSDX文件的页面导出为PNG格式**
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
