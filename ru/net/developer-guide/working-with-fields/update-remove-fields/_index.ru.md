---
title: Обновить, удалить поля
type: docs
weight: 20
url: /ru/net/update-remove-fields/
description: В этом разделе объясняется, как обновлять или удалять поля.
---
## **Обновить поле**
 Aspose.Diagram for .NET позволяет обновлять и удалять[поле](https://reference.aspose.com/diagram/net/aspose.diagram/field) на Microsoft Visio диаграммы из ваших собственных приложений, без автоматизации Microsoft Office.

[Поле](https://reference.aspose.com/diagram/net/aspose.diagram/field) объект представляет собой текстовое поле в[текст](https://reference.aspose.com/diagram/net/aspose.diagram/text) бегать. Свойство поля, представленное[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class поддерживает набор объектов Aspose.Diagram.Field.
### **Образец программирования**
Следующий фрагмент кода обновляет поле в shape.
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

### **Удалить поле**
Следующий фрагмент кода удаляет поле в форме.
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
