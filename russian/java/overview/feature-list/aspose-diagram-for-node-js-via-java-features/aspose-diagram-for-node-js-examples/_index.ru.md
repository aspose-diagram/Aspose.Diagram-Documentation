---
title: Aspose.Diagram для примеров Node.js
type: docs
weight: 10
url: /ru/java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API позволяет работать с диаграммами Visio без какого-либо понимания базового формата файла. Вы можете создавать файлы Visio VSDX с нуля и конвертировать файлы VSDX в PNG всего за пару строк кода.
---
Aspose.Diagram для Node.js прост в использовании и позволяет работать с диаграммами Visio без какого-либо понимания базового формата файла. Вы можете создавать файлы Visio VSDX с нуля, используя простые строки кода. Вы также можете преобразовать файлы VSDX в PNG всего за пару строк кода. В этой статье мы перечислим несколько основных примеров работы с файлами Visio VSDX с использованием Aspose.Diagram для Node.js API.
## **Создайте Visio VSDX с нуля, используя Node.js**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Страница экспорта файла Visio VSDX в формат PNG**
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
