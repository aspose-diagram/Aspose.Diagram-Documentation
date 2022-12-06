---
title: Node.js Örnekleri için Aspose.Diagram
type: docs
weight: 10
url: /tr/java/aspose-diagram-for-node-js-examples/
description: Viso Diagram Node.js API, temeldeki dosya biçimini anlamadan Visio diyagramlarıyla çalışmanıza olanak tanır. Visio VSDX dosyalarını sıfırdan oluşturabilir ve VSDX dosyalarını birkaç satır kodla PNG'ye dönüştürebilirsiniz.
---
Node.js için Aspose.Diagram'in kullanımı kolaydır ve temeldeki dosya biçimini anlamadan Visio diyagramlarıyla çalışmanıza olanak tanır. Basit kod satırlarını kullanarak sıfırdan Visio VSDX dosyaları oluşturabilirsiniz. Ayrıca VSDX dosyalarını birkaç satır kodla PNG'ye dönüştürebilirsiniz. Bu makalede, Node.js API için Aspose.Diagram kullanarak Visio VSDX dosyalarıyla çalışmak için bazı temel örnekleri listeliyoruz.
## **Node.js kullanarak Sıfırdan Visio VSDX oluşturun**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Visio VSDX Dosyasının Sayfasını PNG Formatına Aktar**
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
