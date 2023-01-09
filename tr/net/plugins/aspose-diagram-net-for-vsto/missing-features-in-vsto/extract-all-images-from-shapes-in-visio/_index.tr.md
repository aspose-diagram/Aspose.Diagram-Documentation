---
title: Visio'deki Şekillerdeki Tüm Resimleri Çıkarın
type: docs
weight: 10
url: /tr/net/extract-all-images-from-shapes-in-visio/
---
 bu**Sayfa** Sınıf nesnesi, ön plan sayfasının veya arka plan sayfasının çizim alanını temsil eder. Diagram sınıfı tarafından sunulan Shapes özelliği, Aspose.Diagram.Shape nesnelerinin bir koleksiyonunu destekler. Bu özellik, belirli bir sayfadaki tüm görüntüleri çıkarmak için kullanılabilir.

Aşağıdaki kod parçası, belirli bir sayfadaki tüm görüntüleri çıkarır.

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
## **Örnek Kodu İndir**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
