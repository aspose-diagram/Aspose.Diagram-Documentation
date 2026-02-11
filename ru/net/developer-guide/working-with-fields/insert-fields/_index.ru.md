---
title: Создать, Вставить поля
type: docs
weight: 10
url: /ru/net/create-insert-fields/
description: Как создавать, вставлять поля с помощью C# Diagram API.
---
## **Вставить поле**
 Aspose.Diagram for .NET позволяет создавать и вставлять[поле](https://reference.aspose.com/diagram/net/aspose.diagram/field) на Microsoft Visio диаграммы из ваших собственных приложений, без автоматизации Microsoft Office.
### **Образец программирования**
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
