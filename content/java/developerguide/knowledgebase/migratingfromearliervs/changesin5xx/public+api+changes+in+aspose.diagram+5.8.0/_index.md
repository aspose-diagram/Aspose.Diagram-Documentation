---
title : "Public API Changes in Aspose.Diagram 5.8.0" 
description : "" 
weight : 20081 
toc : false
type: docs
url: /java/developerguide/knowledgebase/migratingfromearliervs/changesin5xx/public+api+changes+in+aspose.diagram+5.8.0/
---

# Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 5.8.0


This document describes changes to the Aspose.Diagram API from version 5.7.0 to 5.8.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behaviour behind the scenes in Aspose.Diagram. 

### SaveToolBar Option is added in the HTMLSaveOptions 

The new `SaveToolBar` option has been added in the `HTMLSaveOptions` class. It specifies whether to save toolbar or not. The default value is true. Example codes:

**Java**

{{< code lang="java" >}}
// initialize HTMLSaveOptions class object
HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option
opts.setSaveToolBar(false);
{{< /code >}}

### VSDX Saving Option is added in the SaveFileFormat 

Previously, Aspose.Diagram API supported reading VSDX format, but now we have added support of writing diagrams in the VSDX format. Example codes:

**Java**

{{< code lang="java" >}}
// save diagram in the VSDX format
diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

### Group Method has been added in the ShapeCollection Class

Developers can now group multiple shapes together in the Visio diagram using Aspose.Diagram API. Example codes:

**Java**

{{< code lang="java" >}}
// load a Visio diagram
Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes
Shape[] shapes = new Shape[2];

// extract and assign shapes to the array
shapes[0] = diagram.getPages().get(0).getShapes().getShape(1);
shapes[1] = diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group
diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram
diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

