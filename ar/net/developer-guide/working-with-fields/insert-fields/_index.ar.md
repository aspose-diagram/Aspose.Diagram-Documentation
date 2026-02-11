---
title: إنشاء وإدراج الحقول
type: docs
weight: 10
url: /ar/net/create-insert-fields/
description: كيفية إنشاء وإدخال الحقول باستخدام C# Diagram API.
---
## **أدخل الحقل**
 يتيح لك Aspose.Diagram for .NET الإنشاء والإدراج[مجال](https://reference.aspose.com/diagram/net/aspose.diagram/field) إلى Microsoft Visio الرسوم البيانية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office.
### **عينة البرمجة**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_InsertField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Insert field
Field fld = new Field();
fld.Value.Val = "1";
shape.Fields.Add(fld);

// Save diagram 
diagram.Save(dataDir + "InsertField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

