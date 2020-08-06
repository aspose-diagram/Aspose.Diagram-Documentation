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
[Event](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Event) class allows developers to set event cells in the ShapeSheet. This help topic demonstrates how developers can set formulas in the event cells:

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-eventsection-SettingEventCells-SettingEventCells.java" >}}
