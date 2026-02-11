---
title: Felder aktualisieren, entfernen
type: docs
weight: 20
url: /de/net/update-remove-fields/
description: In diesem Abschnitt wird erläutert, wie Sie Felder aktualisieren oder entfernen.
---
## **Feld aktualisieren**
 Aspose.Diagram for .NET lässt Sie aktualisieren und entfernen[aufstellen](https://reference.aspose.com/diagram/net/aspose.diagram/field) bis Microsoft Visio Diagramme aus eigenen Applikationen, ohne Microsoft Office Automatisierung.

 Das[Aufstellen](https://reference.aspose.com/diagram/net/aspose.diagram/field) Objekt repräsentiert ein Textfeld in a[Text](https://reference.aspose.com/diagram/net/aspose.diagram/text) Lauf. Die Feldeigenschaft, die durch die verfügbar gemacht wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Field-Objekten.
### **Programmierbeispiel**
Das folgende Stück Codeaktualisierungsfeld in Form.
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

### **Feld entfernen**
Der folgende Codeabschnitt entfernt das Feld in der Form.
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
