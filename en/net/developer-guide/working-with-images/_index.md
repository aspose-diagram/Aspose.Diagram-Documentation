---
title: Working with Images
type: docs
weight: 60
url: /net/working-with-images/
description: This section explains how to insert or get image from a visio page with Aspose.Diagram.
---

## **Extract All Images From a Visio Page**
In Microsoft Visio, pages are either foreground or background pages. You can extract images from a particular page of a Visio file.
### **Extract Images**
The Page Class object represents the drawing area of a foreground page or a background page. The Shapes property exposed by the Diagram class supports a collection of Aspose.Diagram.Shape objects. This property can be used to extract all the images from a particular page.
#### **Extract Images Programming Sample**
The following piece of code extracts all images from a particular Visio page.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Load memory stream into bitmap object
            System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

            // Save bmp here
            bitmap.Save(dataDir + "ExtractAllImages" + shape.ID + "_out.bmp");
        }
    }
}

{{< /highlight >}}
```
## **Get Icons of Various Visio Shapes**
Aspose.Diagram for .NET API now allows developers to get icons of various Visio shapes. 
### **Getting the Shape Icon**
The code in the samples below show how to:

1. Load an existing diagram or stencil.
1. Get master by its index
1. Get master icon. 
1. Save icon to the local space.
#### **Get Icons Programming Sample**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// Get master
Master master = stencil.Masters.GetMaster(1);

using (System.IO.MemoryStream stream = new System.IO.MemoryStream(master.Icon))
{
    // Load memory stream into bitmap object
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);
    // Save as png format
    bitmap.Save(dataDir + "MasterIcon_out.png", System.Drawing.Imaging.ImageFormat.Png);
}

{{< /highlight >}}
```
## **Replace a Picture Shape of the Visio Diagram**
Aspose.Diagram for .NET API allows developers to access and replace available picture shapes in the Visio diagram.
### **Replacing a Picture Shape**
The code in the samples below show how to:

1. Load an existing diagram.
1. Iterate through the selective page shapes.
1. Apply filter to get picture shapes.
1. Save resultant Visio diagram to the local space.
#### **Replace a Picture Shape Programming Sample**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
// Convert image into bytes array
byte[] imageBytes = File.ReadAllBytes(dataDir + "Picture.png");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Replace picture shape
            shape.ForeignData.Value = imageBytes;
        }
    }
}

// Save diagram
diagram.Save(dataDir + "ReplaceShapePicture_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Import Bitmap Image as a Visio Shape**
Aspose.Diagram for .NET API now allows developers to import a bitmap image as a Microsoft Visio shape.
### **Insert a BMP Image in Visio**
The code in the samples below shows how to:

1. Create a diagram.
1. Get Visio page
1. Import a bitmap image as a Visio shape
1. Save the diagram.
#### **Insert a BMP Image Programming Sample**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Create a new diagram
Diagram diagram = new Diagram();

// Get page object by index
Page page0 = diagram.Pages[0];
// Set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import Bitmap image as Visio shape
page0.AddShape(pinX, pinY, width, hieght, new FileStream(dataDir + "image.bmp", FileMode.OpenOrCreate));

// Save Visio diagram
diagram.Save(dataDir + "InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Convert Specified Area of the Visio Page to an Image**
With Aspose.Diagram for .NET API, developers can define an area with XY coordinates, width and height, and then convert this area to a supported image format.
### **Convert Visio drawing area to an Image**
The code in the samples below shows how to:

1. Load an existing Visio drawing
1. Define rectangle area
1. Convert specified area to an image

**C#**

{{< highlight java >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
