+++
title = "Public API Changes in Aspose.Diagram 17.01" 
description = "" 
weight = 20069 
+++

Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 17.01  

# Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 17.01


This document describes changes to the Aspose.Diagram API from version 16.12.0 to 17.01, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behaviour behind the scenes in Aspose.Diagram.

### Convert Visio Drawing with Selective Shapes

Developers can select specific shapes to convert the Visio drawing to any other supported format. We have added Shapes member in the RenderingSaveOptions class for this purpose. Each save option class is the extended form of RenderingSaveOptions class. Please check the code example:

**Java**

{{< code lang="java" >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";
// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.getShapes();
// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.getPages().get(0).getShapes().getShape(1));
shapes.add(diagram.getPages().get(0).getShapes().getShape(2));
// save Visio drawing
diagram.save(dataDir + "SelectiveShapes_out.svg", options);
{{< /code >}}

