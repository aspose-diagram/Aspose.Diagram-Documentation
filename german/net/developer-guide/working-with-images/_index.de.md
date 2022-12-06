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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **Holen Sie sich Symbole in verschiedenen Visio-Formen**
Aspose.Diagram for .NET API ermöglicht es Entwicklern jetzt, Symbole verschiedener Visio Formen zu erhalten.
### **Abrufen des Shape-Symbols**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram oder Schablone.
1. Holen Sie sich den Master anhand seines Index
1. Holen Sie sich das Master-Symbol.
1. Symbol im lokalen Bereich speichern.
#### **Holen Sie sich ein Icon-Programmierbeispiel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **Ersetzen Sie eine Bildform von Visio Diagram**
Aspose.Diagram for .NET API ermöglicht Entwicklern den Zugriff und das Ersetzen verfügbarer Bildformen in Visio diagram.
### **Ersetzen einer Bildform**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Laden Sie eine vorhandene diagram.
1. Iterieren Sie durch die selektiven Seitenformen.
1. Filter anwenden, um Bildformen zu erhalten.
1. Speichern Sie das Ergebnis Visio diagram im lokalen Bereich.
#### **Ersetzen eines Bildform-Programmierbeispiels**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **Bitmap-Bild als Visio-Form importieren**
Aspose.Diagram for .NET API ermöglicht es Entwicklern jetzt, ein Bitmap-Bild als Microsoft Visio Form zu importieren.
### **Insert a BMP Image in Visio**
Der Code in den folgenden Beispielen zeigt, wie Sie:

1. Erstellen Sie eine diagram.
1. Holen Sie sich die Seite Visio
1. Importieren Sie ein Bitmap-Bild als Visio-Form
1. Speichern Sie die diagram.
#### **Insert a BMP Image Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
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
