---
title: Arbeiten mit Bildern
type: docs
weight: 60
url: /de/net/working-with-images/
description: In diesem Abschnitt wird erläutert, wie Sie ein Bild von einer visio-Seite mit Aspose.Diagram einfügen oder abrufen.
---
## **Extrahieren Sie alle Bilder von einer Visio-Seite**
In Microsoft Visio sind Seiten entweder Vorder- oder Hintergrundseiten. Sie können Bilder aus einer bestimmten Seite einer Visio-Datei extrahieren.
### **Bilder extrahieren**
Das Seitenklassenobjekt repräsentiert den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite. Die Shapes-Eigenschaft, die von der Diagram-Klasse bereitgestellt wird, unterstützt eine Sammlung von Aspose.Diagram.Shape-Objekten. Diese Eigenschaft kann verwendet werden, um alle Bilder einer bestimmten Seite zu extrahieren.
#### **Programmierbeispiel für Bilder extrahieren**
Der folgende Codeabschnitt extrahiert alle Bilder von einer bestimmten Visio-Seite.

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
## **Holen Sie sich Symbole in verschiedenen Visio-Formen**
Aspose.Diagram for .NET API ermöglicht es Entwicklern jetzt, Symbole verschiedener Visio Formen zu erhalten.
### **Abrufen des Shape-Symbols**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram oder Schablone.
1. Holen Sie sich den Master anhand seines Index
1. Holen Sie sich das Master-Symbol.
1. Symbol im lokalen Bereich speichern.
#### **Holen Sie sich ein Icon-Programmierbeispiel**
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
## **Ersetzen Sie eine Bildform von Visio Diagram**
Aspose.Diagram for .NET API ermöglicht Entwicklern den Zugriff und das Ersetzen verfügbarer Bildformen in Visio diagram.
### **Ersetzen einer Bildform**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram.
1. Iterieren Sie durch die selektiven Seitenformen.
1. Filter anwenden, um Bildformen zu erhalten.
1. Speichern Sie das Ergebnis Visio diagram im lokalen Bereich.
#### **Ersetzen eines Bildform-Programmierbeispiels**
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
## **Bitmap-Bild als Visio-Form importieren**
Aspose.Diagram for .NET API ermöglicht es Entwicklern jetzt, ein Bitmap-Bild als Microsoft Visio Form zu importieren.
### **Insert a BMP Image in Visio**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Erstellen Sie eine diagram.
1. Holen Sie sich die Seite Visio
1. Importieren Sie ein Bitmap-Bild als Visio-Form
1. Speichern Sie die diagram.
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
## **Wandeln Sie den angegebenen Bereich der Seite Visio in ein Bild um**
Mit Aspose.Diagram for .NET API können Entwickler einen Bereich mit XY-Koordinaten, Breite und Höhe definieren und diesen Bereich dann in ein unterstütztes Bildformat konvertieren.
### **Konvertieren Sie den Zeichenbereich Visio in ein Bild**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene Visio-Zeichnung
1. Rechteckbereich definieren
1. Angegebenen Bereich in ein Bild umwandeln

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
