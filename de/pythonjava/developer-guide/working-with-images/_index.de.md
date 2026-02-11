---
title: Arbeiten mit Bildern
type: docs
weight: 70
url: /de/python-java/working-with-images/
description: Auf dieser Seite wird beschrieben, wie Sie ein Bild aus einer Seite der Zeichnung Visio mit der Bibliothek Aspose.Diagram extrahieren, ersetzen oder einfügen.
---
## **Extrahieren Sie alle Bilder von einer Visio-Seite**
 In Microsoft Visio sind Seiten entweder Vorder- oder Hintergrundseiten. Sie können Bilder von einer bestimmten Seite extrahieren[eine Visio-Datei](ExtractAllImagesFromPage.vsd).
### **Bilder extrahieren**
Das Seitenklassenobjekt repräsentiert den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite. Die Shapes-Eigenschaft, die von der Diagram-Klasse bereitgestellt wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Diese Eigenschaft kann verwendet werden, um alle Bilder einer bestimmten Seite zu extrahieren.
#### **Programmierbeispiel für Bilder extrahieren**
Der folgende Codeabschnitt extrahiert alle Bilder von einer bestimmten Visio-Seite.


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

## **Holen Sie sich Symbole in verschiedenen Visio-Formen**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio Formen](Timeline.vss). 
### **Abrufen des Shape-Symbols**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram oder Schablone.
1. Holen Sie sich den Master anhand seines Index
1. Holen Sie sich das Master-Symbol.
1. Symbol im lokalen Bereich speichern.
#### **Holen Sie sich ein Icon-Programmierbeispiel**

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

## **Ersetzen Sie eine Bildform von Visio Diagram**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [die Visio diagram](ExtractAllImagesFromPage.vsd).
### **Ersetzen einer Bildform**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram.
1. Iterieren Sie durch die selektiven Seitenformen.
1. Filter anwenden, um Bildformen zu erhalten.
1. Speichern Sie das Ergebnis Visio diagram im lokalen Bereich.
#### **Ersetzen eines Bildform-Programmierbeispiels**

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

## **Bild als Visio-Form importieren**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **Fügen Sie ein Bild in Visio ein**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Erstellen Sie eine diagram.
1. Holen Sie sich die Seite Visio
1. Importieren Sie ein Bild als Visio-Form
1. Speichern Sie die diagram.
#### **Fügen Sie ein Beispiel für die Bildprogrammierung ein**

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

