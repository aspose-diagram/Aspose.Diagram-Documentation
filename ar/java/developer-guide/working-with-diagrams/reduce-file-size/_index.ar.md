---
title: تصغير حجم الملف
type: docs
weight: 50
url: /ar/java/reduce-file-size/
description: يشرح هذا القسم كيفية تصغير حجم الملف من diagram إلى Aspose.Diagram.
---
## **تصغير حجم الملف**
 Aspose.Diagram for Java API يسمح للمطورين بإزالة المعلومات المخفية من diagram لتقليل حجم الملف.
 ال[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) يمثل الكائن مساحة الرسم لصفحة أمامية أو صفحة خلفية. لتقليل حجم الملف ، يمكنك استخدام[RemoveHiddenInfoItem](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) خصائص في**RemoveHiddenInformation ()** طريقة[Diagram](https://reference.aspose.com/diagram/java)صف دراسي. يوضح مثال الكود أدناه كيفية إزالة المعلومات المخفية من diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}

