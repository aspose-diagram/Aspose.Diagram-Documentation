+++
title = "Working with Images" 
description = "" 
weight = 8038 
+++

Aspose.Diagram for .NET : Working with Images  

# Aspose.Diagram for .NET : Working with Images


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Extract All Images From a Visio Page](#WorkingwithImages-ExtractAllImagesFromaVisioPage)
    *   1.1 [Extract Images](#WorkingwithImages-ExtractImages)
        *   1.1.1 [Extract Images Programming Sample](#WorkingwithImages-ExtractImagesProgrammingSample)
*   2 [Get Icons of Various Visio Shapes](#WorkingwithImages-GetIconsofVariousVisioShapes)
    *   2.1 [Getting the Shape Icon](#WorkingwithImages-GettingtheShapeIcon)
        *   2.1.1 [Get Icons Programming Sample](#WorkingwithImages-GetIconsProgrammingSample)
*   3 [Replace a Picture Shape of the Visio Diagram](#WorkingwithImages-ReplaceaPictureShapeoftheVisioDiagram)
    *   3.1 [Replacing a Picture Shape](#WorkingwithImages-ReplacingaPictureShape)
        *   3.1.1 [Replace a Picture Shape Programming Sample](#WorkingwithImages-ReplaceaPictureShapeProgrammingSample)
*   4 [Import Bitmap Image as a Visio Shape](#WorkingwithImages-ImportBitmapImageasaVisioShape)
    *   4.1 [Insert a BMP Image in Visio](#WorkingwithImages-InsertaBMPImageinVisio)
        *   4.1.1 [Insert a BMP Image Programming Sample](#WorkingwithImages-InsertaBMPImageProgrammingSample)
*   5 [Convert Specified Area of the Visio Page to an Image](#WorkingwithImages-ConvertSpecifiedAreaoftheVisioPagetoanImage)
    *   5.1 [Convert Visio drawing area to an Image](#WorkingwithImages-ConvertVisiodrawingareatoanImage)
{{< /panel >}}
 

 

## Extract All Images From a Visio Page

In Microsoft Visio, pages are either foreground or background pages. You can extract images from a particular page of a Visio file.

### Extract Images

The Page Class object represents the drawing area of a foreground page or a background page. The Shapes property exposed by the Diagram class supports a collection of Aspose.Diagram.Shape objects. This property can be used to extract all the images from a particular page.

#### Extract Images Programming Sample

The following piece of code extracts all images from a particular Visio page.

## Get Icons of Various Visio Shapes

Aspose.Diagram for .NET API now allows developers to get icons of various Visio shapes. 

### Getting the Shape Icon

The code in the samples below show how to:

1.  Load an existing diagram or stencil.
2.  Get master by its index
3.  Get master icon. 
4.  Save icon to the local space.

#### Get Icons Programming Sample

## Replace a Picture Shape of the Visio Diagram

Aspose.Diagram for .NET API allows developers to access and replace available picture shapes in the Visio diagram.

### Replacing a Picture Shape

The code in the samples below show how to:

1.  Load an existing diagram.
2.  Iterate through the selective page shapes.
3.  Apply filter to get picture shapes.
4.  Save resultant Visio diagram to the local space.

#### Replace a Picture Shape Programming Sample

## Import Bitmap Image as a Visio Shape

Aspose.Diagram for .NET API now allows developers to import a bitmap image as a Microsoft Visio shape.

### Insert a BMP Image in Visio

The code in the samples below shows how to:

1.  Create a diagram.
2.  Get Visio page
3.  Import a bitmap image as a Visio shape
4.  Save the diagram.

#### Insert a BMP Image Programming Sample

## Convert Specified Area of the Visio Page to an Image

With Aspose.Diagram for .NET API, developers can define an area with XY coordinates, width and height, and then convert this area to a supported image format.

### Convert Visio drawing area to an Image

The code in the samples below shows how to:

1.  Load an existing Visio drawing
2.  Define rectangle area
3.  Convert specified area to an image

**C#**

{{< code lang="c#" >}}
// load a Visio drawing
Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");
Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
// specify region with XY coordinates, width and height
Options.Area = new RectangleF(0, 0, 1, 1);
// save into the image format
diagram.Save(@"c:\temp\area.png", Options);
{{< /code >}}

## Attachments:

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Retrieving page information-001.png](https://docs2.aspose.com/diagram/net/attachments/18350198/18546849.png) (image/png)  

