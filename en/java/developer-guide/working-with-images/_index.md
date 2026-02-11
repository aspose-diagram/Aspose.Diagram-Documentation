---
title: Working with Images
type: docs
weight: 70
url: /java/working-with-images/
---

## **Extract All Images From a Visio Page**
In Microsoft Visio, pages are either foreground or background pages. You can extract images from a particular page of a Visio file.
### **Extract Images**
The Page Class object represents the drawing area of a foreground page or a background page. The Shapes property exposed by the Diagram class supports a collection of Aspose.Diagram.Shape objects. This property can be used to extract all the images from a particular page.
#### **Extract Images Programming Sample**
The following piece of code extracts all images from a particular Visio page.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}

## **Get Icons of Various Visio Shapes**
Aspose.Diagram for Java API now allows developers to get icons of various Visio shapes. 
### **Getting the Shape Icon**
The code in the samples below show how to:

1. Load an existing diagram or stencil.
1. Get master by its index
1. Get master icon. 
1. Save icon to the local space.
#### **Get Icons Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetShapeIcon.class);  
// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// get master
Master master = stencil.getMasters().getMasterByName("Triangle");
// get byte array
byte[] bytes = master.getIcon();
// create an image file
FileOutputStream fos = new FileOutputStream(dataDir + "MasterIcon_Out.png");
// write byte array of the image
fos.write(bytes);
// close array
fos.close();

{{< /highlight >}}

## **Replace a Picture Shape of the Visio Diagram**
Aspose.Diagram for Java API allows developers to access and replace available picture shapes in the Visio diagram.
### **Replacing a Picture Shape**
The code in the samples below show how to:

1. Load an existing diagram.
1. Iterate through the selective page shapes.
1. Apply filter to get picture shapes.
1. Save resultant Visio diagram to the local space.
#### **Replace a Picture Shape Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReplaceShapePicture.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
        
// convert image into bytes array       
File fi = new File(dataDir + "Picture.png");
byte[] fileContent = Files.readAllBytes(fi.toPath());
		
// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        //replace picture shape
    	shape.getForeignData().setValue(fileContent);
    }
}

// save diagram
diagram.save(dataDir + "ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Import Bitmap Image as a Visio Shape**
Aspose.Diagram for Java API now allows developers to import a bitmap image as a Microsoft Visio shape.
### **Insert a BMP Image in Visio**
The code in the samples below show how to:

1. Create a diagram.
1. Get Visio page
1. Import a bitmap image as a Visio shape
1. Save the diagram.
#### **Insert a BMP Image Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}

