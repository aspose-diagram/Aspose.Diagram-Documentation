---
title: Lavorare con le immagini
type: docs
weight: 70
url: /it/python-java/working-with-images/
description: Questa pagina descrive come estrarre, sostituire o inserire un'immagine da una pagina del disegno Visio con libreria Aspose.Diagram.
---
## **Estrai tutte le immagini da una pagina Visio**
 In Microsoft Visio, le pagine sono in primo piano o in secondo piano. Puoi estrarre immagini da una particolare pagina di[un fascicolo Visio](ExtractAllImagesFromPage.vsd).
### **Estrai immagini**
L'oggetto Page Class rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Shapes esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Shape. Questa proprietà può essere utilizzata per estrarre tutte le immagini da una determinata pagina.
#### **Estrarre le immagini di esempio di programmazione**
Il seguente pezzo di codice estrae tutte le immagini da una particolare pagina Visio.

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
## **Ottieni icone di varie forme Visio**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio forme](Timeline.vss). 
### **Ottenere l'icona della forma**
Il codice negli esempi seguenti mostra come:

1. Carica uno diagram o uno stencil esistente.
1. Ottieni master dal suo indice
1. Ottieni l'icona principale.
1. Salva l'icona nello spazio locale.
#### **Ottieni un esempio di programmazione delle icone**
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
## **Sostituire una forma immagine del Visio Diagram**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [il Visio diagram](ExtractAllImagesFromPage.vsd).
### **Sostituzione di una forma immagine**
Il codice negli esempi seguenti mostra come:

1. Carica un diagram esistente.
1. Scorri le forme di pagina selettive.
1. Applica il filtro per ottenere le forme dell'immagine.
1. Salva il risultante Visio diagram nello spazio locale.
#### **Sostituire un esempio di programmazione di Picture Shape**
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
## **Importa immagine come forma Visio**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **Inserisci un'immagine in Visio**
Il codice negli esempi seguenti mostra come:

1. Crea uno diagram.
1. Ottenere Visio pagina
1. Importa un'immagine come forma Visio
1. Salva lo diagram.
#### **Inserisci un esempio di programmazione di immagini**
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
