---
title: Извлечь все изображения из фигур в Visio
type: docs
weight: 10
url: /ru/net/extract-all-images-from-shapes-in-visio/
---
**Страница** Объект класса представляет область рисования страницы переднего плана или страницы фона. Свойство Shapes, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Shape. Это свойство можно использовать для извлечения всех изображений с определенной страницы.

Следующий фрагмент кода извлекает все изображения с определенной страницы.

{{< highlight "csharp" >}}

 //Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("ExtractImageFromShape.vsd");

//enter page index i.e. 0 for first one

foreach (Shape shape in diagram.Pages[0].Shapes)

{

	//Filter shapes by type Foreign

	if (shape.Type == Aspose.Diagram.TypeValue.Foreign)

	{

		using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))

		{

			//Load memory stream into bitmap object

			System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

			// save bmp here

			bitmap.Save("ExtractedShape" + shape.ID + ".bmp");

		}

	}

}

{{< /highlight >}}
## **Скачать пример кода**
- [Битбакет](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
