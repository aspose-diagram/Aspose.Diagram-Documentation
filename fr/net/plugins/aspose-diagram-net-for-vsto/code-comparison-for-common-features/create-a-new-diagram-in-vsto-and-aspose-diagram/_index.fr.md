---
title: Créer un nouveau Diagram dans VSTO et Aspose.Diagram
type: docs
weight: 110
url: /fr/net/create-a-new-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
VSTO vous permet de programmer avec les fichiers Microsoft Visio. Pour créer un nouveau diagram :

1. Créez un objet d'application Visio.
1. Rendre l'objet d'application invisible.
1. Créez un diagram vide.
1. Ajoutez des formes à partir des maîtres Visio (pochoirs).
1. Enregistrez le fichier sous VDX.

{{< highlight "csharp" >}}

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

{{< /highlight >}}
### **Aspose.Diagram**
Lors de la programmation avec Aspose.Diagram, vous n'avez pas besoin de Microsoft Visio sur la machine et vous pouvez travailler indépendamment de Microsoft Office Automation. Pour créer un nouveau diagram :

1. Créez un diagram vide.
1. Ajoutez des formes à partir des maîtres Visio (pochoirs).
1. Enregistrez le fichier sous VDX.

{{< highlight "csharp" >}}

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


{{< /highlight >}}
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/asposemarketplace/Aspose_for_VSTO/tree/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Create%20a%20New%20Diagram)
- [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Create%20a%20New%20Diagram%20%28Aspose.Diagram%29.zip/download)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Create%20a%20New%20Diagram/)
