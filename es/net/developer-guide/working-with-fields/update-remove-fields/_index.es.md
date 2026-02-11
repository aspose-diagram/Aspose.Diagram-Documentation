---
title: Actualizar, eliminar campos
type: docs
weight: 20
url: /es/net/update-remove-fields/
description: Esta sección explica cómo actualizar o eliminar campos.
---
## **Actualizar campo**
 Aspose.Diagram for .NET le permite actualizar y eliminar[campo](https://reference.aspose.com/diagram/net/aspose.diagram/field) a Microsoft Visio diagramas desde dentro de sus propias aplicaciones, sin Microsoft Office Automatización.

 los[Campo](https://reference.aspose.com/diagram/net/aspose.diagram/field) objeto representa un campo de texto en un[texto](https://reference.aspose.com/diagram/net/aspose.diagram/text) correr. La propiedad de campo, expuesta por la[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase admite una colección de objetos Aspose.Diagram.Field.
### **Ejemplo de programación**
El siguiente fragmento de código actualiza el campo en forma.

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


### **Eliminar campo**
El siguiente fragmento de código elimina el campo en forma.

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

