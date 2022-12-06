---
title: Formen gruppieren, konvertieren und überprüfen
type: docs
weight: 50
url: /de/java/group-convert-and-verify-shapes/
---
## **Gruppieren Sie mehrere Formen in der Zeichnung Visio**
Aspose.Diagram API ermöglicht es Entwicklern, Formen zu gruppieren, um sie alle auf einmal zu verschieben. Jede Form in einer Gruppe behält eine eindeutige Identität bei und hat ihre eigenen Eigenschaften. Wenn wir die Formatierung einer Gruppe von Formen ändern, weist sie jeder Form die neue Eigenschaft zu.
### **So gruppieren Sie Formen**
Die Group-Methode, die von der ShapeCollection-Klasse verfügbar gemacht wird, kann verwendet werden, um Formen zu gruppieren.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. initialisierte ein Array der Formen
1. Holen Sie sich eine bestimmte Form nach ID.
1. Holen Sie sich eine andere bestimmte bestimmte Form nach ID.
1. Weisen Sie dem Array Shapes zu.
1. gruppieren Sie Shapes, indem Sie die Group-Methode aufrufen.
1. außer diagram
#### **Programmierbeispiel für Gruppenformen**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um Formen mit Aspose.Diagram for Java API zu gruppieren.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GroupShapes-GroupShapes.java" >}}
## **Konvertieren Sie eine Visio-Form in andere Dateiformate**
Aspose.Diagram for Java API ermöglicht es Entwicklern, eine einzelne Visio-Form in jedes andere unterstützte Dateiformat zu konvertieren. In diesem Artikel entfernen wir alle anderen Visio-Shapes von der Seite und passen die Seiteneinstellungen entsprechend der Quell-Shape-Größe an.
### **Konvertieren einer bestimmten Visio-Form**
 Entwickler können eine Visio-Form in PDF, HTML, Bild, SVG und SWF konvertieren[Angabe der Visio Speicheroptionen]().
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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.java" >}}
### **Konvertieren Sie Visio Form in PDF**
Die ToPdf-Methode der Shape-Klasse ermöglicht es, eine Form in das PDF-Format zu konvertieren.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Konvertieren Sie Visio Shape in HTML**
Die ToHTML-Methode der Shape-Klasse ermöglicht es, eine Form in das HTML-Format zu konvertieren.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}} 
## **Überprüfen Sie, ob zwei Visio-Formen verbunden oder geklebt sind**
 Mit Aspose.Diagram for Java API können Entwickler überprüfen, ob die beiden Formen Visio verklebt oder verbunden sind. Zuvor haben wir in diesen Hilfethemen gesehen, wie wir zwei Formen verbinden oder kleben können:[Visio Formen hinzufügen und verbinden](/diagram/de/java/add-and-connect-visio-shapes/) und[Kleben Sie Formen in den Behälter](/diagram/de/java/working-with-shapes-gluing/).
### **Überprüfung der verbundenen oder geklebten Formen**
 Das[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Die Klasse bietet IsGlued- und IsConnected-Eigenschaften, um zu bestimmen, ob zwei Shapes geklebt oder verbunden sind.
#### **Programmierbeispiel für verbundene oder geklebte Formen**
Der folgende Codeabschnitt überprüft, ob zwei Shapes verbunden oder geklebt sind.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.java" >}}
## **Überprüfen Sie, ob sich die Form Visio in einer Gruppe von Formen befindet**
Mit Aspose.Diagram for Java API können Entwickler überprüfen, ob sich die Form Visio in einer Gruppe von Formen befindet oder nicht.
### **Überprüfung der Form in der Gruppe der Formen**
Die Shape-Klasse bietet IsInGroup-Eigenschaften, um zu bestimmen, ob sich das Visio-Shape in einem Gruppen-Shape befindet.
#### **Überprüfung der Form in der Gruppe von Formen Programmierbeispiel**
Der folgende Codeabschnitt überprüft, ob sich das Shape in einem Gruppen-Shape befindet.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.java" >}}

{{% alert color="primary" %}} 

 Wir freuen uns über Ihre Fragen und Anregungen unter[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Wir antworten umgehend.

{{% /alert %}}
