---
title: Uppdatera, ta bort fält
type: docs
weight: 20
url: /sv/net/update-remove-fields/
description: Det här avsnittet förklarar hur du uppdaterar eller tar bort fält.
---
## **Uppdatera fält**
 Aspose.Diagram for .NET låter dig uppdatera och ta bort[fält](https://reference.aspose.com/diagram/net/aspose.diagram/field) till Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation.

 De[Fält](https://reference.aspose.com/diagram/net/aspose.diagram/field) objekt representerar textfält i en[text](https://reference.aspose.com/diagram/net/aspose.diagram/text) springa. Fältegenskapen, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass stöder en samling Aspose.Diagram.Field-objekt.
### **Programmeringsexempel**
Följande koduppdateringsfält i form.
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

### **Ta bort fält**
Följande kodbit tar bort fält i form.
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
