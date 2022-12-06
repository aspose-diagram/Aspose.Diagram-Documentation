---
title: Aktualisieren Sie die Formeigenschaften in VSTO und Aspose.Diagram
type: docs
weight: 20
url: /de/net/update-shape-properties-in-vsto-and-aspose-diagram/
---
VSTO

Mit VSTO können Sie mit Microsoft Visio-Dateien programmieren. So aktualisieren Sie Formeigenschaften:

1. Erstellen Sie ein Visio-Anwendungsobjekt.
1. Machen Sie das Anwendungsobjekt unsichtbar.
1. Öffnen Sie eine vorhandene Visio VSD-Datei.
1. Finden Sie die gewünschte Form.
1. Aktualisieren Sie die Formeigenschaften (Text, Textstil, Position und Größe).
1. Speichern Sie die Datei als VDX.

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
Beim Programmieren mit Aspose.Diagram benötigen Sie Microsoft Visio nicht an der Maschine und können unabhängig von Microsoft Office Automation arbeiten. So aktualisieren Sie Formeigenschaften mit Aspose.Diagram for .NET:

1. Öffnen Sie eine vorhandene Visio VSD-Datei.
1. Finden Sie die gewünschte Form.
1. Aktualisieren Sie die Formeigenschaften (Text, Textstil, Position und Größe).
1. Speichern Sie die Datei als VDX.

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
## **Beispielcode herunterladen**
- [GitHub](https://github.com/asposemarketplace/Aspose_for_VSTO/tree/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties)
- [Quellenschmiede](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties%20%28Aspose.Diagram%29.zip/download)
- [Bit Bucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties/)
