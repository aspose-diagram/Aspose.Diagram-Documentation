---
title: Uppdatera formegenskaper i VSTO och Aspose.Diagram
type: docs
weight: 20
url: /sv/net/update-shape-properties-in-vsto-and-aspose-diagram/
---
VSTO

VSTO låter dig programmera med Microsoft Visio filer. Så här uppdaterar du formegenskaper:

1. Skapa ett Visio applikationsobjekt.
1. Gör applikationsobjektet osynligt.
1. Öppna en befintlig Visio VSD fil.
1. Hitta den önskade formen.
1. Uppdatera formegenskaperna (text, textstil, position och storlek).
1. Spara filen som VDX.

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
Vid programmering med Aspose.Diagram behöver du inte Microsoft Visio på maskinen, och du kan arbeta oberoende av Microsoft Office Automation. Så här uppdaterar du formegenskaper med Aspose.Diagram for .NET:

1. Öppna en befintlig Visio VSD fil.
1. Hitta den önskade formen.
1. Uppdatera formegenskaperna (text, textstil, position och storlek).
1. Spara filen som VDX.

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
## **Ladda ner exempelkod**
- [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/tree/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties)
- [Sourceforge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties%20%28Aspose.Diagram%29.zip/download)
- [Bit hink](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties/)
