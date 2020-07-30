---
title : "Create a New Diagram in VSTO and Aspose.Diagram" 
description : "" 
weight : 16105 
toc : false
type: docs
url: /net/plugins/vsto/codecomparison/create+a+new+diagram+in+vsto+and+aspose.diagram/
---

# Aspose.Diagram for .NET : Create a New Diagram in VSTO and Aspose.Diagram


## VSTO

VSTO lets you program with Microsoft Visio files. To create a new diagram:

1.  Create a Visio application object.
2.  Make the application object invisible.
3.  Create an empty diagram.
4.  Add shapes from Visio masters (stencils).
5.  Save the file as VDX.

{{< code lang="cs" >}}
Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
	//Create Visio Application Object
	vdxApp = Application;

	//Make Visio Application Invisible
	vdxApp.Visible = false;

	//Create a new diagram
	vdxDoc = vdxApp.Documents.Add("Drawing.vsd");

	//Load Visio Stencil
	Visio.Documents visioDocs = vdxApp.Documents;
	//-----------//
	Visio.Document visioStencil = visioDocs.OpenEx("sample.vss",
		(short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

	//Set active page
	Visio.Page visioPage = vdxApp.ActivePage;

	//Add a new rectangle shape
	Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
	Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
	visioRectShape.Text = @"Rectangle text.";

	//Add a new star shape
	Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
	Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
	visioStarShape.Text = @"Star text.";

	//Add a new hexagon shape
	Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
	Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
	visioHexagonShape.Text = @"Hexagon text.";


	//Save diagram as VDX
	vdxDoc.SaveAs("Drawing1.vdx");
}
catch (Exception ex)
{
	Console.WriteLine(ex.Message);
}
finally
{
	//Close active document and quit
	vdxDoc.Close();
	vdxApp.Quit();
}
{{< /code >}}

### Aspose.Diagram

When programming with Aspose.Diagram, you do not need Microsoft Visio on the machine, and you can work independently of Microsoft Office Automation. To create a new diagram:

1.  Create an empty diagram.
2.  Add shapes from Visio masters (stencils).
3.  Save the file as VDX.

{{< code lang="cs" >}}
string visioStencil ="sample.vss";
// Create a new diagram
Diagram diagram = new Diagram(visioStencil);

//Add a new rectangle shape
long shapeId = diagram.AddShape(
	4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

//Add a new star shape
shapeId = diagram.AddShape(
	2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

//Add a new hexagon shape
shapeId = diagram.AddShape(
7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

//Save the new diagram
diagram.Save("Drawing1.vdx", SaveFileFormat.VDX);

{{< /code >}}

## Download Sample Code

*   [Codeplex](https://asposevsto.codeplex.com/downloads/get/772932)
*   [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/6/Create.a.New.Diagram.Aspose.Diagram.zip)
*   [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Create%20a%20New%20Diagram%20(Aspose.Diagram).zip/download)
*   [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Create%20a%20New%20Diagram%20(Aspose.Diagram).zip)

