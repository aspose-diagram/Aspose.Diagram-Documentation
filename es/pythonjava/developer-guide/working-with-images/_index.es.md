---
title: Trabajar con imágenes
type: docs
weight: 70
url: /es/python-java/working-with-images/
description: Esta página describe cómo extraer, reemplazar o insertar una imagen de una página del dibujo Visio con la biblioteca Aspose.Diagram.
---
## **Extraiga todas las imágenes de una página Visio**
 En Microsoft Visio, las páginas son páginas de primer plano o de fondo. Puede extraer imágenes de una página particular de[un archivo Visio](ExtractAllImagesFromPage.vsd).
### **Extraer imágenes**
El objeto Clase de página representa el área de dibujo de una página de primer plano o una página de fondo. La propiedad Shapes expuesta por la clase Diagram admite una colección de objetos Aspose.Diagram.Shape. Esta propiedad se puede utilizar para extraer todas las imágenes de una página en particular.
#### **Muestra de programación de extracción de imágenes**
El siguiente fragmento de código extrae todas las imágenes de una página Visio en particular.

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
## **Obtener íconos de varias formas Visio**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio formas](Timeline.vss). 
### **Obtener el icono de forma**
El código de los ejemplos siguientes muestra cómo:

1. Cargue un diagram o plantilla existente.
1. Obtener maestro por su índice
1. Obtener icono maestro.
1. Guardar icono en el espacio local.
#### **Muestra de Programación de Obtener Iconos**
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
## **Reemplace una forma de imagen del Visio Diagram**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [el Visio diagram](ExtractAllImagesFromPage.vsd).
### **Sustitución de una forma de imagen**
El código de los ejemplos siguientes muestra cómo:

1. Cargue un diagram existente.
1. Iterar a través de las formas de página selectivas.
1. Aplicar filtro para obtener formas de imagen.
1. Guarde el Visio diagram resultante en el espacio local.
#### **Reemplazar una muestra de programación de forma de imagen**
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
## **Importar imagen como forma Visio**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **Insertar una imagen en Visio**
El código de los ejemplos siguientes muestra cómo:

1. Crea un diagram.
1. Obtener Visio página
1. Importar una imagen como forma Visio
1. Guarda el diagram.
#### **Insertar una muestra de programación de imágenes**
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
