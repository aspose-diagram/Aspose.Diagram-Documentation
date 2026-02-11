---
title: تحديث وإزالة الحقول
type: docs
weight: 20
url: /ar/net/update-remove-fields/
description: يشرح هذا القسم كيفية تحديث الحقول أو إزالتها.
---
## **تحديث الميدان**
 يتيح لك Aspose.Diagram for .NET التحديث والإزالة[مجال](https://reference.aspose.com/diagram/net/aspose.diagram/field) إلى Microsoft Visio الرسوم البيانية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office.

 ال[مجال](https://reference.aspose.com/diagram/net/aspose.diagram/field) يمثل الكائن حقل نص في ملف[نص](https://reference.aspose.com/diagram/net/aspose.diagram/text) يجري. خاصية الحقل ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة تدعم مجموعة من Aspose.Diagram.Field كائنات.
### **عينة البرمجة**
الجزء التالي من حقل تحديث التعليمات البرمجية في الشكل.
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UpdateField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Get field
Field fld = shape.Fields[0];
//Update format of field
fld.Format.Val = "";
fld.Format.Ufev.Unit = MeasureConst.Undefined;
fld.Format.Ufev.F = "";

//Update value of field
fld.Value.Val = "1";
fld.Value.Ufev.F = "";
fld.Value.Ufev.Unit = MeasureConst.Undefined;

// Save diagram 
diagram.Save(dataDir + "UpdateField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

### **إزالة الحقل**
الجزء التالي من التعليمات البرمجية يزيل الحقل في الشكل.
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_RemoveField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Get field
Field fld = shape.Fields[0];
//Remove field
shape.Fields.Remove(fld);

// Save diagram 
diagram.Save(dataDir + "RemoveField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
