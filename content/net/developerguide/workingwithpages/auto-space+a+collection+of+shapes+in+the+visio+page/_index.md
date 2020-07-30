---
title : "Auto-space a Collection of Shapes in the Visio Page" 
description : "" 
weight : 12034 
toc : false
type: docs
url: /net/developerguide/workingwithpages/auto-space+a+collection+of+shapes+in+the+visio+page/
---

# Aspose.Diagram for .NET : Auto-space a Collection of Shapes in the Visio Page


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Auto-space a Collection of Shapes in the Visio Page](#auto-space-a-collection-of-shapes-in-the-visio-page)
    *   1.1 [Auto-space Shapes in the Page](#auto-space-shapes-in-the-page)
{{< /panel >}}
 

 

## Auto-space a Collection of Shapes in the Visio Page

With Aspose.Diagram for .NET API, developers can auto-space a collection of shapes in the Visio drawing. In order to achieve this, the Page class offers AutoSpaceShapes member which takes ShapeCollection and AutoSpaceOptions parameters. The AutoSpaceOptions class allows to set horizontal and vertical distances.

### Auto-space Shapes in the Page

Use the following code in your .NET application to auto-space a collection of shapes in any page of the Visio drawing.

**C#**

{{< code lang="c#" >}}
// load a Visio drawing
Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");
// get page of the Visio drawing
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// initialize auto space options
AutoSpaceOptions options = new AutoSpaceOptions();
// set horizontal and vertical distances
options.DistanceInHorizontal = 2;
options.DistanceInVertical = 2;
// set auto space 
page.AutoSpaceShapes(page.Shapes, options);
// save Visio drawing
diagram.Save(@"c:\temp\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

## Attachments:

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Retrieving page information-001.png](https://docs2.aspose.com/diagram/net/attachments/50269043/50528296.png) (image/png)  

