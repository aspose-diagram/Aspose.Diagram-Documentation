---
title: Working with Images
type: docs
weight: 70
url: /python-java/working-with-images/
description: This page describes how to extract, replace or insert an image from a page of the Visio drawing with Aspose.Diagram library.
---

## **Extract All Images From a Visio Page**
In Microsoft Visio, pages are either foreground or background pages. You can extract images from a particular page of [a Visio file](ExtractAllImagesFromPage.vsd).
### **Extract Images**
The Page Class object represents the drawing area of a foreground page or a background page. The Shapes property exposed by the Diagram class supports a collection of Aspose.Diagram.Shape objects. This property can be used to extract all the images from a particular page.
#### **Extract Images Programming Sample**
The following piece of code extracts all images from a particular Visio page.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call a Diagram class constructor to load a VSD diagram
diagram = Diagram("ExtractAllImagesFromPage.vsd")

# Enter page index i.e. 0 for first one
for shape in diagram.getPages().getPage(0).getShapes():
    # Filter shapes by type Foreign
    if shape.getType() == TypeValue.FOREIGN:
        fos = java.io.FileOutputStream("ExtractAllImages" + str(shape.getID()) + "_Out.bmp")
        fos.write(shape.getForeignData().getValue())
        fos.close()

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Get Icons of Various Visio Shapes**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio shapes](Timeline.vss). 
### **Getting the Shape Icon**
The code in the samples below show how to:

1. Load an existing diagram or stencil.
1. Get master by its index
1. Get master icon. 
1. Save icon to the local space.
#### **Get Icons Programming Sample**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load stencil file to a diagram object
stencil = Diagram("Timeline.vss")
# get master
master = stencil.getMasters().getMasterByName("Triangle milestone")
# get byte array
icon_bytes = master.getIcon()
# create an image file
fos = java.io.FileOutputStream("MasterIcon_Out.png")
# write byte array of the image
fos.write(icon_bytes)
# close array
fos.close()
jpype.shutdownJVM()

{{< /highlight >}}
```
## **Replace a Picture Shape of the Visio Diagram**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [the Visio diagram](ExtractAllImagesFromPage.vsd).
### **Replacing a Picture Shape**
The code in the samples below show how to:

1. Load an existing diagram.
1. Iterate through the selective page shapes.
1. Apply filter to get picture shapes.
1. Save resultant Visio diagram to the local space.
#### **Replace a Picture Shape Programming Sample**
```
{{< highlight "python" >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# call a Diagram class constructor to load the VSD diagram
diagram = Diagram("ExtractAllImagesFromPage.vsd")

# convert image into bytes array       
fi = java.io.File("image.png")
fileContent = java.nio.file.Files.readAllBytes(fi.toPath())

# Enter page index i.e. 0 for first one
for shape in diagram.getPages().getPage(0).getShapes():
    # Filter shapes by type Foreign
    if shape.getType() == TypeValue.FOREIGN:
        # replace picture shape
        shape.getForeignData().setValue(fileContent)

# save diagram
diagram.save("ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX)
jpype.shutdownJVM()

{{< /highlight >}}
```
## **Import Image as a Visio Shape**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **Insert a Image in Visio**
The code in the samples below show how to:

1. Create a diagram.
1. Get Visio page
1. Import a image as a Visio shape
1. Save the diagram.
#### **Insert a Image Programming Sample**
```
{{< highlight "python" >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Create a new diagram
diagram = Diagram()

# Get page object by index
page0 = diagram.getPages().getPage(0)
# Set pinX, pinY, width and height
pinX = 2
pinY = 2
width = 4
height = 3

# Import Bitmap image as Visio shape
page0.addShape(pinX, pinY, width, height, java.io.FileInputStream("image.png"))

# Save Visio diagram
diagram.save("InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
