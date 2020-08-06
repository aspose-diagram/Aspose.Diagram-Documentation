---
title: Public API Changes in Aspose.Diagram 17.01
type: docs
weight: 10
url: /net/public-api-changes-in-aspose-diagram-17-01/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 16.12.0 to 17.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

{{% /alert %}} 
### **Convert Visio Drawing with Selective Shapes**
Developers can select specific shapes to convert the Visio drawing to any other supported format. We have added [Shapes](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions/properties/shapes) member in the [RenderingSaveOptions](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions) class for this purpose. Each save option class is the extended form of RenderingSaveOptions class. Please check the code example:

**C#**

{{< highlight csharp >}}

 // the path to the documents directory.

string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.Add(diagram.Pages[0].Shapes.GetShape(1));

shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing

diagram.Save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
