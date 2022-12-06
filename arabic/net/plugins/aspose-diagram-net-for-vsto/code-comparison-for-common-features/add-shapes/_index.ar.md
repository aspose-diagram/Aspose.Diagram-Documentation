---
title: أضف الأشكال
type: docs
weight: 30
url: /ar/net/add-shapes/
---
## **VSTO Visio**
{{< highlight "csharp" >}}

 Visio.Application vsdApp = null;

Visio.Document vsdDoc = null;

//Create Visio Application Object

vsdApp = Application;

//Make Visio Application Invisible

vsdApp.Visible = false;

//Create a document object and load a diagram

vsdDoc = vsdApp.Documents.Open("Add Shapes.vdx");

Visio.Documents visioDocs = this.Application.Documents;

Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",

	(short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenDocked);

Visio.Page visioPage = this.Application.ActivePage;

Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");

Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);

visioRectShape.Text = @"Rectangle text.";

Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");

Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);

visioStarShape.Text = @"Star text.";

Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");

Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);

visioHexagonShape.Text = @"Hexagon text.";

{{< /highlight >}}
### **Aspose.Diagram**
{{< highlight "csharp" >}}

 // Load masters from any existing diagram, stencil or template

// and add in the new diagram

string visioStencil = "Add Shapes.vdx";

//Names of the masters present in the stencil

string rectangleMaster = @"Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

// Create a new diagram

Diagram diagram = new Diagram(visioStencil);

//Add a new rectangle shape

long rectangleId = diagram.AddShape(

	pinX, pinY, width, height, rectangleMaster, pageNumber);

//Save the diagram

diagram.Save("Add Shapes.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **تنزيل نموذج التعليمات البرمجية**
- [جيثب](https://github.com/asposemarketplace/Aspose_for_VSTO/wiki/Add-Shapes)
- [سورس فورج](https://sourceforge.net/p/asposevsto/wiki/Home/)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/wiki/Add%20Shapes)
