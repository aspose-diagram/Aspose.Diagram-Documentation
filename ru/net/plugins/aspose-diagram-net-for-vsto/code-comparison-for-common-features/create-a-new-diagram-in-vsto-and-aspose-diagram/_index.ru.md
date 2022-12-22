---
title: Создайте новый Diagram в VSTO и Aspose.Diagram
type: docs
weight: 110
url: /ru/net/create-a-new-diagram-in-vsto-and-aspose-diagram/
---
## **ВСТО**
VSTO позволяет программировать Microsoft Visio файлов. Чтобы создать новый diagram:

1. Создайте объект приложения Visio.
1. Сделать объект приложения невидимым.
1. Создайте пустой diagram.
1. Добавьте формы из мастеров Visio (трафареты).
1. Сохраните файл как VDX.

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
При программировании с Aspose.Diagram вам не нужно Microsoft Visio на машине, и вы можете работать независимо от Microsoft Office Автоматика. Чтобы создать новый diagram:

1. Создайте пустой diagram.
1. Добавьте формы из мастеров Visio (трафареты).
1. Сохраните файл как VDX.

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
## **Скачать пример кода**
- [Гитхаб](https://github.com/asposemarketplace/Aspose_for_VSTO/tree/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Create%20a%20New%20Diagram)
- [Источникфорж](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Create%20a%20New%20Diagram%20%28Aspose.Diagram%29.zip/download)
- [Битбакет](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/Create%20a%20New%20Diagram/)
