---
title: Setting Cells in the Event Section of ShapeSheet
type: docs
weight: 10
url: /java/setting-cells-in-the-event-section-of-shapesheet/
---

{{% alert color="primary" %}} 

Using Aspose.Diagram API, developers can define how a shape responds to specific user actions by writing Visio formulas that handle events automatically. Whenever the user performs one of the actions described as below, the formula in the corresponding ShapeSheet cell is evaluated.

- **TheText** - An event element that is evaluated when a shape's text or text composition changes.
- **EventXFMod** - The shape's position, size, or orientation on the page is changed.
- **EventDblClick** - The shape is double-clicked.
- **EventDrop** - A new instance is created by pasting, duplicating, or dragging a shape, or by dragging and dropping a master.
- **EventMultiDrop** - when multiple new instances are created by pasting, duplicating, or dragging a shape, or by dragging and dropping a master.
- **TheData** - Reserved for future use.

{{% /alert %}} 
## **Setting Event Cells**
[Event](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) class allows developers to set event cells in the ShapeSheet. This help topic demonstrates how developers can set formulas in the event cells:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SettingEventCells.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// get page
Page page = diagram.getPages().get(0);
// get shape id
long shapeId = page.addShape(3.0, 3.0, 0.36, 0.36, "Square");
// get shape
Shape shape = page.getShapes().getShape(shapeId);

// set event cells in the ShapeSheet
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");

// save diagram
diagram.save(dataDir + "Output_NET.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
