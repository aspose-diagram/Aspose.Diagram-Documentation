---
title: Create, Insert fields
type: docs
weight: 10
url: /net/create-insert-fields/
description: How to create, insert fields using C# Diagram API .
---

## **Insert field**
Aspose.Diagram for .NET lets you create and insert [field](https://reference.aspose.com/diagram/net/aspose.diagram/field) to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 
### **Programming Sample**

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

