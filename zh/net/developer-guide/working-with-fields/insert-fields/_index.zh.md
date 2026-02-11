---
title: 创建、插入字段
type: docs
weight: 10
url: /zh/net/create-insert-fields/
description: 如何使用 C# Diagram API 创建、插入字段。
---
## **插入字段**
Aspose.Diagram for .NET 让你创建和插入[场地](https://reference.aspose.com/diagram/net/aspose.diagram/field)从您自己的应用程序到 Microsoft Visio 图表，没有 Microsoft Office 自动化。
### **编程范例**
```
{{< highlight "csharp" >}}
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
```
