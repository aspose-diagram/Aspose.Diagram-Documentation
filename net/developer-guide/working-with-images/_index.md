---
title: Working with Images
type: docs
weight: 60
url: /net/working-with-images/
---

## **Extract All Images From a Visio Page**
In Microsoft Visio, pages are either foreground or background pages. You can extract images from a particular page of a Visio file.
### **Extract Images**
The Page Class object represents the drawing area of a foreground page or a background page. The Shapes property exposed by the Diagram class supports a collection of Aspose.Diagram.Shape objects. This property can be used to extract all the images from a particular page.
#### **Extract Images Programming Sample**
The following piece of code extracts all images from a particular Visio page.

{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **Get Icons of Various Visio Shapes**
Aspose.Diagram for .NET API now allows developers to get icons of various Visio shapes. 
### **Getting the Shape Icon**
The code in the samples below show how to:

1. Load an existing diagram or stencil.
1. Get master by its index
1. Get master icon. 
1. Save icon to the local space.
#### **Get Icons Programming Sample**
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **Replace a Picture Shape of the Visio Diagram**
Aspose.Diagram for .NET API allows developers to access and replace available picture shapes in the Visio diagram.
### **Replacing a Picture Shape**
The code in the samples below show how to:

1. Load an existing diagram.
1. Iterate through the selective page shapes.
1. Apply filter to get picture shapes.
1. Save resultant Visio diagram to the local space.
#### **Replace a Picture Shape Programming Sample**
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **Import Bitmap Image as a Visio Shape**
Aspose.Diagram for .NET API now allows developers to import a bitmap image as a Microsoft Visio shape.
### **Insert a BMP Image in Visio**
The code in the samples below shows how to:

1. Create a diagram.
1. Get Visio page
1. Import a bitmap image as a Visio shape
1. Save the diagram.
#### **Insert a BMP Image Programming Sample**
{{< gist "aspose-diagram" "cce69e51f567ea17ef24bc35fef0f689" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
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
