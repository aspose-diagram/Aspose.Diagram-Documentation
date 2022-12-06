---
title: Extrahera alla bilder från former i Visio
type: docs
weight: 10
url: /sv/net/extract-all-images-from-shapes-in-visio/
---
 De**Sida** Klassobjekt representerar ritytan på en förgrundssida eller en bakgrundssida. Shapes-egenskapen som exponeras av klassen Diagram stöder en samling Aspose.Diagram.Shape-objekt. Den här egenskapen kan användas för att extrahera alla bilder från en viss sida.

Följande kodbit extraherar alla bilder från en viss sida.

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
## **Ladda ner exempelkod**
- [Bit hink](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
