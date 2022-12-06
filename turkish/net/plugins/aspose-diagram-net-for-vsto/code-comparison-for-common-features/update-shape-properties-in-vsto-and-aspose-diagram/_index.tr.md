---
title: VSTO ve Aspose.Diagram'de şekil özelliklerini güncelleyin
type: docs
weight: 20
url: /tr/net/update-shape-properties-in-vsto-and-aspose-diagram/
---
VSTO

VSTO, Microsoft Visio dosyalarıyla programlama yapmanızı sağlar. Şekil özelliklerini güncellemek için:

1. Bir Visio uygulama nesnesi oluşturun.
1. Uygulama nesnesini görünmez yapın.
1. Mevcut bir Visio VSD dosyasını açın.
1. Gerekli şekli bulun.
1. Şekil özelliklerini (metin, metin stili, konum ve boyut) güncelleyin.
1. Dosyayı VDX olarak kaydedin.

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
Aspose.Diagram ile programlama yaparken makinede Microsoft Visio'e gerek yok Microsoft Office Otomasyondan bağımsız çalışabilirsiniz. Aspose.Diagram for .NET ile şekil özelliklerini güncellemek için:

1. Mevcut bir Visio VSD dosyasını açın.
1. Gerekli şekli bulun.
1. Şekil özelliklerini (metin, metin stili, konum ve boyut) güncelleyin.
1. Dosyayı VDX olarak kaydedin.

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
## **Örnek Kodu İndir**
- [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/tree/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties)
- [kaynak forge](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties%20%28Aspose.Diagram%29.zip/download)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Update%20shape%20properties/)
