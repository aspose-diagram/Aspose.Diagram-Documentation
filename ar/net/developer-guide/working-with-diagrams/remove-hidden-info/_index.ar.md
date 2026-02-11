---
title: إزالة المعلومات المخفية
type: docs
weight: 50
url: /ar/net/remove-hidden-info/
description: يشرح هذا القسم كيفية إزالة المعلومات غير المستخدمة أو المخفية من diagram مع Aspose.Diagram.
---
## **إزالة المعلومات المخفية**
 Aspose.Diagram for .NET API يسمح للمطورين بإزالة المعلومات المخفية من diagram. لإزالة المعلومات المخفية ، يمكنك استخدام**RemoveHiddenInfoItem** خصائص في**RemoveHiddenInformation ()**طريقة Diagram فئة. يوضح مثال الكود أدناه كيفية رسم إزالة المعلومات المخفية من diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();
// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Remove hidden information from diagram
diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));
// Initialize HTML save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Save the Visio diagram
diagram.Save(dataDir + "RemoveHiddenInfo_out.html", options);

{{< /highlight >}}
```
