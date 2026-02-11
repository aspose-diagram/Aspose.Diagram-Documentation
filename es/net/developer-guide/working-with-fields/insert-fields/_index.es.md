---
title: Crear, Insertar campos
type: docs
weight: 10
url: /es/net/create-insert-fields/
description: Cómo crear, inserte campos usando C# Diagram API .
---
## **Insertar campo**
 Aspose.Diagram for .NET le permite crear e insertar[campo](https://reference.aspose.com/diagram/net/aspose.diagram/field) a Microsoft Visio diagramas desde dentro de sus propias aplicaciones, sin Microsoft Office Automatización.
### **Ejemplo de programación**
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
