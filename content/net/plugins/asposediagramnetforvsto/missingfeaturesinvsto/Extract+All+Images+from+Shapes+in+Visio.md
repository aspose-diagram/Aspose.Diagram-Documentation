+++
title = "Extract All Images from Shapes in Visio" 
description = "" 
weight = 16107 
+++

Aspose.Diagram for .NET : Extract All Images from Shapes in Visio  

# Aspose.Diagram for .NET : Extract All Images from Shapes in Visio


The **Page** Class object represents the drawing area of a foreground page or a background page. The Shapes property exposed by the Diagram class supports a collection of Aspose.Diagram.Shape objects. This property can be used to extract all the images from a particular page.

The following piece of code extracts all the images from a particular page.

{{< code lang="cs" >}}
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
{{< /code >}}

## Download Sample Code

*   [Codeplex](http://goo.gl/KxosuA)
*   [Github](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/10/ExtractAllImagesFromVisio.Aspose.Diagram.zip)
*   [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/ExtractAllImagesFromVisio%20%28Aspose.Diagram%29.zip)

