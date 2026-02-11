---
title: 更新、删除字段
type: docs
weight: 20
url: /zh/net/update-remove-fields/
description: 本节说明如何更新或删除字段。
---
## **更新字段**
Aspose.Diagram for .NET 让你更新和删除[场地](https://reference.aspose.com/diagram/net/aspose.diagram/field)从您自己的应用程序到 Microsoft Visio 图表，没有 Microsoft Office 自动化。

这[场地](https://reference.aspose.com/diagram/net/aspose.diagram/field)object 表示 a 中的文本字段[文本](https://reference.aspose.com/diagram/net/aspose.diagram/text)跑。字段属性，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类支持 Aspose.Diagram.Field 对象的集合。
### **编程范例**
下面这段代码更新字段的形状。

{{< highlight csharp >}}
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


### **删除字段**
以下代码段删除形状中的字段。

{{< highlight csharp >}}
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

