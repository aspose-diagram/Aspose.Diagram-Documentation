---
title: دمج الجمع Diagram
type: docs
weight: 30
url: /ar/net/merge-combine-diagram/
description: يشرح هذا القسم كيفية دمج ملف visio
---
## **سيناريوهات الاستخدام الممكنة**

 Aspose.Diagram يسمح لك بدمج ملفين visio في ملف واحد.
 Aspose.Diagram for .NET API لديه[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تمثل رسم Visio.
باستخدام الطريقة[**يجمع**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/methods/combine) في[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة لدمج الرسوم البيانية.

## **عينة من الرموز**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Load another Visio diagram
Diagram diagram2 = new Diagram(Drawing2.vsdx");
diagram2.Combine(diagram);

// Save the new Visio
newDiagram.Save(dataDir + "out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

