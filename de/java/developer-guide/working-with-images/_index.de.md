---
title: Arbeiten mit Bildern
type: docs
weight: 70
url: /de/java/working-with-images/
---
## **Extrahieren Sie alle Bilder von einer Visio-Seite**
In Microsoft Visio sind Seiten entweder Vorder- oder Hintergrundseiten. Sie können Bilder aus einer bestimmten Seite einer Visio-Datei extrahieren.
### **Bilder extrahieren**
Das Seitenklassenobjekt repräsentiert den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite. Die Shapes-Eigenschaft, die von der Diagram-Klasse bereitgestellt wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Diese Eigenschaft kann verwendet werden, um alle Bilder einer bestimmten Seite zu extrahieren.
#### **Programmierbeispiel für Bilder extrahieren**
Der folgende Codeabschnitt extrahiert alle Bilder von einer bestimmten Visio-Seite.


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

## **Holen Sie sich Symbole in verschiedenen Visio-Formen**
Aspose.Diagram for Java API ermöglicht es Entwicklern jetzt, Symbole verschiedener Visio Formen zu erhalten.
### **Abrufen des Shape-Symbols**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram oder Schablone.
1. Holen Sie sich den Master anhand seines Index
1. Holen Sie sich das Master-Symbol.
1. Symbol im lokalen Bereich speichern.
#### **Holen Sie sich ein Icon-Programmierbeispiel**

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

## **Ersetzen Sie eine Bildform von Visio Diagram**
Aspose.Diagram for Java API ermöglicht Entwicklern den Zugriff und das Ersetzen verfügbarer Bildformen in Visio diagram.
### **Ersetzen einer Bildform**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram.
1. Iterieren Sie durch die selektiven Seitenformen.
1. Filter anwenden, um Bildformen zu erhalten.
1. Speichern Sie das Ergebnis Visio diagram im lokalen Bereich.
#### **Ersetzen eines Bildform-Programmierbeispiels**

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

## **Bitmap-Bild als Visio-Form importieren**
Aspose.Diagram for Java API ermöglicht es Entwicklern jetzt, ein Bitmap-Bild als Microsoft Visio Form zu importieren.
### **Insert a BMP Image in Visio**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Erstellen Sie eine diagram.
1. Holen Sie sich die Seite Visio
1. Importieren Sie ein Bitmap-Bild als Visio-Form
1. Speichern Sie die diagram.
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

