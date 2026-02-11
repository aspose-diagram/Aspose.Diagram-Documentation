---
title: دمج الجمع Diagram
type: docs
weight: 30
url: /ar/java/merge-combine-diagram/
description: يشرح هذا القسم كيفية دمج ملف visio
---
## **سيناريوهات الاستخدام الممكنة**

 Aspose.Diagram يسمح لك بدمج ملفين visio في ملف واحد.
 Aspose.Diagram for Java API لديه[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) فئة تمثل رسم Visio.
باستخدام الطريقة[**يجمع**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#combine(com.aspose.diagram.Diagram) ) في[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) فئة لدمج الرسوم البيانية.

## **عينة من الرموز**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CombineDiagram.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(dataDir + Drawing2.vsdx");

diagram2.combine(diagram);

// save in the VSDX format
diagram.save(dataDir + "CombineDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

