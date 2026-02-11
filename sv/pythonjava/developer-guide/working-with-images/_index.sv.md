---
title: Arbeta med bilder
type: docs
weight: 70
url: /sv/python-java/working-with-images/
description: Den här sidan beskriver hur man extraherar, ersätter eller infogar en bild från en sida i Visio-ritningen med Aspose.Diagram-biblioteket.
---
## **Extrahera alla bilder från en Visio-sida**
 I Microsoft Visio är sidorna antingen förgrunds- eller bakgrundssidor. Du kan extrahera bilder från en viss sida i[en Visio fil](ExtractAllImagesFromPage.vsd).
### **Extrahera bilder**
Sidklassobjektet representerar ritytan på en förgrundssida eller en bakgrundssida. Shapes-egenskapen som exponeras av klassen Diagram stöder en samling Aspose.Diagram.Shape-objekt. Den här egenskapen kan användas för att extrahera alla bilder från en viss sida.
#### **Extrahera bilder Programmeringsexempel**
Följande kodbit extraherar alla bilder från en viss Visio-sida.

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
## **Få ikoner av olika Visio former**
 Aspose.Diagram för Python via Java API tillåter nu utvecklare att få ikoner för olika[Visio former](Timeline.vss). 
### **Få formikonen**
Koden i exemplen nedan visar hur man:

1. Ladda en befintlig diagram eller stencil.
1. Få mästare efter dess index
1. Få master ikon.
1. Spara ikonen till det lokala utrymmet.
#### **Få ikoner programmering exempel**
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
## **Byt ut en bildform på Visio Diagram**
 Aspose.Diagram för Python via Java API låter utvecklare komma åt och ersätta tillgängliga bildformer i[Visio diagram](ExtractAllImagesFromPage.vsd).
### **Byta ut en bildform**
Koden i exemplen nedan visar hur man:

1. Ladda ett befintligt diagram.
1. Iterera genom de selektiva sidformerna.
1. Använd filter för att få bildformer.
1. Spara resulterande Visio diagram till det lokala utrymmet.
#### **Byt ut ett bildformsprogrammeringsprov**
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
## **Importera bild som en Visio Shape**
Aspose.Diagram för Python via Java API tillåter nu utvecklare att importera en bild som en Microsoft Visio form.
### **Infoga en bild i Visio**
Koden i exemplen nedan visar hur man:

1. Skapa ett diagram.
1. Skaffa Visio sida
1. Importera en bild som en Visio-form
1. Spara diagram.
#### **Infoga ett bildprogrammeringsexempel**
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
