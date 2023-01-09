---
title: Estrai tutte le immagini dalle forme in Visio
type: docs
weight: 10
url: /it/net/extract-all-images-from-shapes-in-visio/
---
 Il**Pagina** L'oggetto classe rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Shapes esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Shape. Questa proprietà può essere utilizzata per estrarre tutte le immagini da una determinata pagina.

Il seguente pezzo di codice estrae tutte le immagini da una particolare pagina.

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
## **Scarica il codice di esempio**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
