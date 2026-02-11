---
title: تغيير حجم الصفحة
type: docs
weight: 10
url: /ar/java/change-page-size/
description: يشرح هذا القسم كيفية تغيير حجم الصفحة في ملف visio باستخدام Aspose.Diagram.
---
## **تغيير حجم الصفحة**

 ال[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات.
 ال[PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) يمثل الكائن سمات الصفحة ، مثل عرض الصفحة وارتفاعها ومقياسها. يمكن استخدام هذه الخاصية لتغيير حجم الصفحة.

استخدم خاصية PageProps لتغيير حجم الصفحة.
### **تعيين عينة برمجة حجم الصفحة**
قطعة الكود التالية تغير حجم الصفحة من diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

