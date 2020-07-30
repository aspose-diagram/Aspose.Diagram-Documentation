---
title : "Auto-space a Collection of Shapes in the Visio Page" 
description : "" 
weight : 12028 
toc : false
type: docs
url: /java/developerguide/workingwithpages/auto-space+a+collection+of+shapes+in+the+visio+page/
---

# Aspose.Diagram for Java : Auto-space a Collection of Shapes in the Visio Page


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Auto-space a Collection of Shapes in the Visio Page](#auto-space-a-collection-of-shapes-in-the-visio-page)
    *   1.1 [Auto-space Shapes in the Page](#auto-space-shapes-in-the-page)
{{< /panel >}}
 

 

## Auto-space a Collection of Shapes in the Visio Page

With Aspose.Diagram for Java API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the Page class offers autoSpaceShapes member which takes ShapeCollection and AutoSpaceOptions parameters. The AutoSpaceOptions class allows to set horizontal and vertical distances.

### Auto-space Shapes in the Page

Use the following code in your Java application to auto-space a collection of shapes in any page of the Visio drawing.

**Java**

{{< code lang="java" >}}
// load a Visio drawing
Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");
// get page of the Visio drawing
Page page = diagram.getPages().getPage("Page-1");
// initialize auto space options
AutoSpaceOptions options = new AutoSpaceOptions();
// set horizontal and vertical distances
options.setDistanceInHorizontal(2);
options.setDistanceInVertical(2);
// set auto space 
page.autoSpaceShapes(page.getShapes(), options);
// save Visio drawing
diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

