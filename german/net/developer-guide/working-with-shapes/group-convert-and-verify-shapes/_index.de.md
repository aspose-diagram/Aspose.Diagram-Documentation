---
title: Formen gruppieren, konvertieren und überprüfen
type: docs
weight: 80
url: /de/net/group-convert-and-verify-shapes/
description: In diesem Abschnitt wird erläutert, wie Sie Formen mit Aspose.Diagram gruppieren.
---
## **Gruppieren Sie mehrere Formen in der Zeichnung Visio**
Aspose.Diagram API ermöglicht es Entwicklern, Formen zu gruppieren, um sie alle auf einmal zu verschieben. Jede Form in einer Gruppe behält eine eindeutige Identität bei und hat ihre eigenen Eigenschaften. Wenn wir die Formatierung einer Gruppe von Formen ändern, weist sie jeder Form die neue Eigenschaft zu.
### **So gruppieren Sie Formen**
 Die Gruppenmethode, die durch die ausgesetzt ist[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) Klasse kann verwendet werden, um Formen zu gruppieren.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. initialisierte ein Array der Formen
1. Holen Sie sich eine bestimmte Form nach ID.
1. Holen Sie sich eine andere bestimmte bestimmte Form nach ID.
1. Weisen Sie dem Array Shapes zu.
1. gruppieren Sie Shapes, indem Sie die Group-Methode aufrufen.
1. außer diagram
#### **Programmierbeispiel für Gruppenformen**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um Formen mit Aspose.Diagram for .NET API zu gruppieren.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
## **Konvertieren Sie eine Visio-Form in andere Dateiformate**
Aspose.Diagram for .NET API ermöglicht es Entwicklern, eine einzelne Visio-Form in jedes andere unterstützte Dateiformat zu konvertieren. In diesem Artikel entfernen wir alle anderen Visio-Shapes von der Seite und passen die Seiteneinstellungen entsprechend der Quell-Shape-Größe an.
### **Konvertieren einer bestimmten Visio-Form**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by **Angabe der Visio Speicheroptionen**.
Dieser Beispielcode funktioniert wie folgt:

1. Laden Sie eine Quelle Visio.
1. Holen Sie sich eine bestimmte Seite.
1. Entfernen Sie die Hintergrundseite.
1. Erstellen Sie eine Hash-Tabelle aller Formen, die die IDs und Namen enthalten.
1. Durchlaufen Sie die Hash-Tabelle
1. Entfernen Sie alle Formen von der Seite Visio, außer der bestimmten.
1. Legen Sie die Seitengröße fest.
1. Speichern Sie die Seite Visio in einem beliebigen unterstützten Dateiformat.
#### **Konvertieren Sie Shape-Programmierbeispiel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Überprüfen Sie, ob zwei Visio-Formen verbunden oder geklebt sind**
 Mit Aspose.Diagram for .NET API können Entwickler überprüfen, ob die beiden Formen Visio verklebt oder verbunden sind. Zuvor haben wir in diesen Hilfethemen gesehen, wie wir zwei Formen verbinden oder kleben können:[Visio Formen hinzufügen und verbinden](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) und[Kleben Sie Formen in den Behälter](/diagram/de/net/working-with-shapes-gluing/).
### **Überprüfung der verbundenen oder geklebten Formen**
 Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Die Klasse bietet IsGlued- und IsConnected-Eigenschaften, um zu bestimmen, ob zwei Shapes geklebt oder verbunden sind.
#### **Programmierbeispiel für verbundene oder geklebte Formen**
Der folgende Codeabschnitt überprüft, ob zwei Shapes verbunden oder geklebt sind.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **Überprüfen Sie, ob sich die Form Visio in einer Gruppe von Formen befindet**
Mit Aspose.Diagram for .NET API können Entwickler überprüfen, ob sich die Form Visio in einer Gruppe von Formen befindet oder nicht.
### **Überprüfung der Form in der Gruppe der Formen**
Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)-Klasse bietet IsInGroup-Eigenschaften, um zu bestimmen, ob sich das Visio-Shape in einem Gruppen-Shape befindet.
#### **Überprüfung der Form in der Gruppe von Formen Programmierbeispiel**
Der folgende Codeabschnitt überprüft, ob sich das Shape in einem Gruppen-Shape befindet.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
