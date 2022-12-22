---
title: Extraiga todas las imágenes de las formas en Visio
type: docs
weight: 10
url: /es/net/extract-all-images-from-shapes-in-visio/
---
 los**Página** El objeto de clase representa el área de dibujo de una página de primer plano o una página de fondo. La propiedad Shapes expuesta por la clase Diagram admite una colección de objetos Aspose.Diagram.Shape. Esta propiedad se puede utilizar para extraer todas las imágenes de una página en particular.

El siguiente fragmento de código extrae todas las imágenes de una página en particular.

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
## **Descargar código de muestra**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
