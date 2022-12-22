---
title: استخراج كافة الصور من الأشكال في Visio
type: docs
weight: 10
url: /ar/net/extract-all-images-from-shapes-in-visio/
---
 ال**صفحة** يمثل كائن الفئة منطقة الرسم لصفحة أمامية أو صفحة خلفية. تدعم خاصية الأشكال المعروضة بواسطة الفئة Diagram مجموعة من Aspose.Diagram كائنات الشكل. يمكن استخدام هذه الخاصية لاستخراج جميع الصور من صفحة معينة.

يستخرج جزء الكود التالي جميع الصور من صفحة معينة.

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
## **تنزيل نموذج التعليمات البرمجية**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
