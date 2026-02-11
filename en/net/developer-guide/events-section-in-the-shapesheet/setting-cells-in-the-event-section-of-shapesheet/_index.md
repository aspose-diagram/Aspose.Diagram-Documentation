---
title: Setting Cells in the Event Section of ShapeSheet
type: docs
weight: 10
url: /net/setting-cells-in-the-event-section-of-shapesheet/
description: Manage event properties of visio files.
---

{{% alert color="primary" %}} 

Using Aspose.Diagram API, developers can define how a shape responds to specific user actions by writing Visio formulas that handle events automatically. Whenever the user performs one of the four actions described as below, the formula in the corresponding ShapeSheet cell is evaluated.

- **TheText** - An event element that is evaluated when a shape's text or text composition changes.
- **EventXFMod** - The shape's position, size, or orientation on the page is changed.
- **EventDblClick** - The shape is double-clicked.
- **EventDrop** - A new instance is created by pasting, duplicating, or dragging a shape, or by dragging and dropping a master.
- **EventMultiDrop** - when multiple new instances are created by pasting, duplicating, or dragging a shape, or by dragging and dropping a master.
- **TheData** - Reserved for future use.

{{% /alert %}} 
## **Setting Event Cells**
[Event](https://reference.aspose.com/diagram/net/aspose.diagram/event) class allows developers to set event cells in the ShapeSheet. This help topic demonstrates how developers can set formulas in the event cells:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_EventSection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);
// Get shape id
long shapeId = page.AddShape(3.0, 3.0, 0.36, 0.36, "Square");
// Get shape
Aspose.Diagram.Shape shape = page.Shapes.GetShape(shapeId);

// Set event cells in the ShapeSheet
shape.Event.EventXFMod.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDblClick.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventMultiDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheText.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheData.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";

// Save diagram
diagram.Save(dataDir + "SettingCellsInEventSection_out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
