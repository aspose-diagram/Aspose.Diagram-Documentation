---
title: Extrahieren Sie alle Bilder aus Shapes in Visio
type: docs
weight: 10
url: /de/net/extract-all-images-from-shapes-in-visio/
---
 Das**Buchseite** Das Klassenobjekt repräsentiert den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite. Die Shapes-Eigenschaft, die von der Diagram-Klasse bereitgestellt wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Diese Eigenschaft kann verwendet werden, um alle Bilder einer bestimmten Seite zu extrahieren.

Der folgende Codeabschnitt extrahiert alle Bilder von einer bestimmten Seite.

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
## **Beispielcode herunterladen**
- [Bit Bucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
