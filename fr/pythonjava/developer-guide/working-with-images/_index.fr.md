---
title: Travailler avec des images
type: docs
weight: 70
url: /fr/python-java/working-with-images/
description: Cette page décrit comment extraire, remplacer ou insérer une image d'une page du dessin Visio avec la bibliothèque Aspose.Diagram.
---
## **Extraire toutes les images d'une page Visio**
 Dans Microsoft Visio, les pages sont soit des pages de premier plan, soit des pages d'arrière-plan. Vous pouvez extraire des images d'une page particulière de[un dossier Visio](ExtractAllImagesFromPage.vsd).
### **Extraire des images**
L'objet Page Class représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Shapes exposée par la classe Diagram prend en charge une collection d'objets Aspose.Diagram.Shape. Cette propriété peut être utilisée pour extraire toutes les images d'une page particulière.
#### **Exemple de programmation d'extraction d'images**
Le morceau de code suivant extrait toutes les images d'une page Visio particulière.


{{< highlight python >}}
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

## **Obtenez des icônes de diverses formes Visio**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio formes](Timeline.vss). 
### **Obtenir l'icône de forme**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram ou un gabarit existant.
1. Obtenir le maître par son index
1. Obtenir l'icône principale.
1. Enregistrer l'icône dans l'espace local.
#### **Obtenir un exemple de programmation d'icônes**

{{< highlight python >}}
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

## **Remplacer une forme d'image du Visio Diagram**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [le Visio diagram](ExtractAllImagesFromPage.vsd).
### **Remplacement d'une forme d'image**
Le code dans les exemples ci-dessous montre comment :

1. Chargez un diagram existant.
1. Parcourez les formes de page sélectives.
1. Appliquer le filtre pour obtenir des formes d'image.
1. Enregistrez le résultat Visio diagram dans l'espace local.
#### **Remplacer un exemple de programmation de forme d'image**

{{< highlight python >}}
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

## **Importer l'image en tant que forme Visio**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **Insérer une image dans Visio**
Le code dans les exemples ci-dessous montre comment :

1. Créez un diagram.
1. Obtenir la page Visio
1. Importer une image en tant que forme Visio
1. Enregistrez le diagram.
#### **Insérer un exemple de programmation d'image**

{{< highlight python >}}
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

