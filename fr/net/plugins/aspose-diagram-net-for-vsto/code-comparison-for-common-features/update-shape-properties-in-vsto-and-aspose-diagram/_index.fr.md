---
title: Mettre à jour les propriétés de forme dans VSTO et Aspose.Diagram
type: docs
weight: 20
url: /fr/net/update-shape-properties-in-vsto-and-aspose-diagram/
---
VSTO

VSTO vous permet de programmer avec les fichiers Microsoft Visio. Pour mettre à jour les propriétés de la forme :

1. Créez un objet d'application Visio.
1. Rendre l'objet d'application invisible.
1. Ouvrez un fichier Visio VSD existant.
1. Trouvez la forme requise.
1. Mettez à jour les propriétés de la forme (texte, style de texte, position et taille).
1. Enregistrez le fichier sous VDX.

{{< highlight "csharp" >}}

 Visio.Application vsdApp = null;

Visio.Document vsdDoc = null;

try

{

	//Create Visio Application Object

	vsdApp = Application;

	//Make Visio Application Invisible

	vsdApp.Visible = false;

	//Create a document object and load a diagram

	vsdDoc = vsdApp.Documents.Open( "Drawing.vsd");

	//Create page object to get required page

	Visio.Page page = vsdApp.ActivePage;

	//Create shape object to get required shape

	Visio.Shape shape = page.Shapes["Process1"];

	//Set shape text and text style

	shape.Text = "Hello World";

	shape.TextStyle = "CustomStyle1";

	//Set shape's position

	shape.get_Cells("PinX").ResultIU = 5;

	shape.get_Cells("PinY").ResultIU = 5;

	//Set shape's height and width

	shape.get_Cells("Height").ResultIU = 2;

	shape.get_Cells("Width").ResultIU = 3;

	//Save file as VDX

	vsdDoc.SaveAs("Drawing1.vdx");

}

catch (Exception ex)

{

	Console.WriteLine(ex.Message);

}

finally

{

	//Close active document and quit

	vsdDoc.Close();

	vsdApp.Quit();

}


{{< /highlight >}}
### **Aspose.Diagram**
Lors de la programmation avec Aspose.Diagram, vous n'avez pas besoin de Microsoft Visio sur la machine et vous pouvez travailler indépendamment de Microsoft Office Automation. Pour mettre à jour les propriétés de la forme avec Aspose.Diagram for .NET :

1. Ouvrez un fichier Visio VSD existant.
1. Trouvez la forme requise.
1. Mettez à jour les propriétés de la forme (texte, style de texte, position et taille).
1. Enregistrez le fichier sous VDX.

{{< highlight "csharp" >}}

 	//Save the uploaded file as PDF

	Diagram diagram = new Diagram("Drawing1.vsd");

	//Find a particular shape and update its properties

	foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)

	{

		if (shape.Name.ToLower() == "process1")

		{

			shape.Text.Value.Clear();

			shape.Text.Value.Add(new Txt("Hello World"));

			//Find custom style sheet and set as shape's text style

			foreach (StyleSheet styleSheet in diagram.StyleSheets)

			{

				if (styleSheet.Name == "CustomStyle1")

				{

					shape.TextStyle = styleSheet;

				}

			}

			//Set horizontal and vertical position of the shape

			shape.XForm.PinX.Value = 5;

			shape.XForm.PinY.Value = 5;

			//Set height and width of the shape

			shape.XForm.Height.Value = 2;

			shape.XForm.Width.Value = 3;

		}

	}

	//Save shape as VDX

	diagram.Save("Drawing1.vdx", SaveFileFormat.VDX);

}

catch (Exception ex)

{

	Console.WriteLine(ex.Message);

}


{{< /highlight >}}
## **Télécharger l'exemple de code**
- [GithubGenericName](https://github.com/asposemarketplace/Aspose_for_VSTO/tree/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties)
- [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties%20%28Aspose.Diagram%29.zip/download)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties/)
