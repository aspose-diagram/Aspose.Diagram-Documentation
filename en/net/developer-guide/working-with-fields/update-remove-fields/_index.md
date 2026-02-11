---
title: Update,Remove Fields
type: docs
weight: 20
url: /net/update-remove-fields/
description: This section explains how to update or remve fields.
---

## **Update Field**
Aspose.Diagram for .NET lets you update and remove [field](https://reference.aspose.com/diagram/net/aspose.diagram/field) to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

The [Field](https://reference.aspose.com/diagram/net/aspose.diagram/field) object represents text field in a [text](https://reference.aspose.com/diagram/net/aspose.diagram/text) run. The field property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class supports a collection of Aspose.Diagram.Field objects.
### **Programming Sample**
The following piece of code update field in shape.

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


### **Remove Field**
The following piece of code remove field in shape.

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

