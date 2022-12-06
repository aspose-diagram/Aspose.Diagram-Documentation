---
title: Extraire toutes les images des formes dans Visio
type: docs
weight: 10
url: /fr/net/extract-all-images-from-shapes-in-visio/
---
 La**Page** L'objet de classe représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Shapes exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Shape. Cette propriété peut être utilisée pour extraire toutes les images d'une page particulière.

Le morceau de code suivant extrait toutes les images d'une page particulière.

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
## **Télécharger l'exemple de code**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
