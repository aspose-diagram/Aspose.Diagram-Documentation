---
title: تحقق من توسيع الصفحة تلقائيًا
type: docs
weight: 10
url: /ar/java/check-page-autoexpand/
description: يشرح هذا القسم كيفية التحقق أو تغيير الصفحة التي يتم توسيعها تلقائيًا في ملف visio مع Aspose.Diagram.
---
## **تحقق من الصفحة AutoExpand**

 ال[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات.
 ال[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) يمثل الكائن سمات الصفحة ، مثل عرض الصفحة وارتفاعها ومقياسها. يمكن استخدام هذه الخاصية للتحقق من التوسيع التلقائي للصفحة.

استخدم خاصية PageProps للتحقق من التوسيع التلقائي للصفحة.
### **تحقق من نموذج برمجة التوسيع التلقائي للصفحة**
التوسيع التلقائي لصفحة التحقق من الرمز التالي من diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

