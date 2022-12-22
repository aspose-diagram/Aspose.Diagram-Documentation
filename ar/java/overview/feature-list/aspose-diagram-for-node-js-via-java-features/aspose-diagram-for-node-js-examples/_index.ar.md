---
title: Aspose.Diagram لأمثلة Node.js
type: docs
weight: 10
url: /ar/java/aspose-diagram-for-node-js-examples/
description: يتيح لك Viso Diagram Node.js API العمل باستخدام الرسوم التخطيطية Visio دون أي فهم لتنسيق الملف الأساسي. يمكنك إنشاء Visio VSDX ملفات من البداية وتحويل ملفات VSDX إلى PNG ببضع سطرين من التعليمات البرمجية.
---
Aspose.Diagram لـ Node.js سهل الاستخدام ويتيح لك العمل مع الرسوم التخطيطية Visio دون أي فهم لتنسيق الملف الأساسي. يمكنك إنشاء ملفات Visio VSDX من البداية باستخدام سطور بسيطة من التعليمات البرمجية. يمكنك أيضًا تحويل ملفات VSDX إلى PNG ببضع سطرين من التعليمات البرمجية. في هذه المقالة ، ندرج بعض الأمثلة الأساسية للعمل مع ملفات Visio VSDX باستخدام Aspose.Diagram لـ Node.js API.
## **قم بإنشاء Visio VSDX من سكراتش باستخدام Node.js**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **تصدير صفحة من Visio VSDX ملف إلى تنسيق PNG**
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
