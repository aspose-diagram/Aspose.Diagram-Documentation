---
title: Arbeiten mit Text
type: docs
weight: 90
url: /de/net/working-with-text/
description: In diesem Abschnitt wird erläutert, wie Sie eine Textform einfügen oder den Text der Form mit Aspose.Diagram aktualisieren.
---
## **Fügen Sie eine Textform in die Seite Visio ein**
 Mit Aspose.Diagram API können Entwickler überall auf der Visio-Seite eine Textform einfügen. Um dies zu erreichen, wird die AddText-Methode des[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Die Klasse nimmt PinX-, PinY-, Breiten-, Höhen- und Textparameter an.
### **Fügen Sie ein Textform-Programmierbeispiel ein**
Der folgende Codeabschnitt fügt eine Textform in Visio diagram hinzu.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-InsertTextShape-InsertTextShape.cs" >}}
## **Aktualisieren Sie Visio Shape-Text**
 Ebenso gut wie[Diagramme erstellen](/diagram/de/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET lässt Sie auf unterschiedliche Weise mit Formen arbeiten. In diesem Artikel wird beschrieben, wie Sie auf Text in Formen zugreifen und ihn aktualisieren. Die Text-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützt das Objekt Aspose.Diagram.Text. Die Eigenschaft kann verwendet werden, um den Text einer Form abzurufen oder zu aktualisieren. Der Vorgang zum Aktualisieren des Texts einer Form ist unkompliziert:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Legen Sie den neuen Text fest.
1. Speichern Sie die diagram.
### **Programmierbeispiel für Formtext aktualisieren**
Der folgende Codeabschnitt aktualisiert den Text einer Form. Shapes werden anhand ihrer IDs identifiziert. Die folgenden Codesegmente suchen nach einer Form namens process und mit der ID 1 und ändern ihren Text.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-UpdateShapeText-UpdateShapeText.cs" >}}
## **Wenden Sie ein integriertes oder benutzerdefiniertes Stylesheet auf eine Visio-Form an**
Microsoft Visio Stylesheets speichern Formatierungsinformationen, die für ein konsistentes Erscheinungsbild auf Formen angewendet werden können. Mit Aspose.Diagram for .NET können Sie Stylesheets aus einer Anwendung heraus anwenden.

 Die Eigenschaften TextStyle, FillStyle und LineStyle, die von der bereitgestellt werden[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse unterstützt die[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) Objekt. Die Eigenschaft kann verwendet werden, um Stilinformationen abzurufen und benutzerdefinierte Text-, Linien- und Füllstile auf einen diagram anzuwenden.
### **Benutzerdefinierte Stile unter Microsoft Visio**
So wenden Sie benutzerdefinierte Stile auf Formen in Microsoft Visio an:

1. Öffnen Sie eine diagram in Microsoft Visio.
1.  Auswählen**Stile definieren** von dem**Format** Menü (Visio 2007), oder klicken Sie mit der rechten Maustaste**Stile** in dem**Zeichnungs-Explorer** Fenster und wählen Sie aus**Stile definieren** (Visio 2010).
1.  In dem**Stile definieren** Geben Sie im Dialogfeld einen neuen Namen für Ihr benutzerdefiniertes Stylesheet ein. Beispiel: CustomStyle1.
1.  Drücke den**Text**, **Linie** und**Füllen** Schaltflächen zum Festlegen von Text-, Linien- und Füllstilen.
1.  Klicken**OK**.

Nachdem Sie benutzerdefinierte Stylesheets in Microsoft Visio definiert haben, verwenden Sie den folgenden Code in einer .NET-Anwendung, um benutzerdefinierte Stile auf Ihre Formen anzuwenden. Beachten Sie, dass die folgenden Codebeispiele das oben definierte benutzerdefinierte Stylesheet aufrufen: Sie müssen den Namen und den Speicherort des angewendeten Sheets kennen. So wenden Sie benutzerdefinierte Stile programmgesteuert an:

1. Laden Sie eine diagram.
1. Suchen Sie die Form, auf die Sie einen Stil anwenden möchten.
1. Laden Sie das Stylesheet.
1. Stile anwenden.
1. Speichern Sie die diagram.
#### **Wenden Sie das Programmierbeispiel für benutzerdefinierte Stile an**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.cs" >}}
## **Wenden Sie einen anderen Stil auf die einzelnen Textwerte einer Form an**
 Ebenso gut wie[Diagramme erstellen](/diagram/de/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET lässt Sie auf unterschiedliche Weise mit Formen arbeiten. Dieser Artikel hilft beim Hinzufügen mehrerer Textwerte zu einer Form und beim Anwenden eines anderen Stils auf jeden Textwert.

{{% alert color="primary" %}} 

Das Shape-Element enthält ein Element namens Text, das die Zeichen des Textes und spezielle Elemente (cp, pp, tp und fld) enthält, die das Ende eines Laufs und den Beginn des nächsten markieren. Char-Element enthält die Formatierungsattribute für den Text der Form, z. B. Schriftart, Farbe, Textstil, Groß-/Kleinschreibung, Position relativ zur Grundlinie und Punktgröße.

{{% /alert %}} 
### **Hinzufügen von Formtext und -stilen**

|**Geben Sie diagram ein**|
|:- |
|![todo: Bild_alt_Text](working-with-text_1.png)|


|**Diagram nach dem Hinzufügen verschiedener Textwerte zu einer Form mit unterschiedlichem Stil für jeden Textwert**|
|:- |
|![todo: Bild_alt_Text](working-with-text_2.png)|
#### **Hinzufügen von Text und Stilen Programmierbeispiel**
Der folgende Codeabschnitt fügt den Text einer Form und verschiedene Stile hinzu.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyFontOnText-ApplyFontOnText.cs" >}}
## **Suchen und ersetzen Sie den Text einer Form**
 Das[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Mit der Klasse können Sie den Text der Form bearbeiten. Die Replace-Methode, verfügbar gemacht durch die[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Klasse, unterstützen Sie das Ändern des Textes einer Form.
Die Codebeispiele in diesem Artikel suchen und ersetzen den Text der Form auf der Seite.

|**Geben Sie diagram ein**|
|:- |
|![todo: Bild_alt_Text](working-with-text_3.png)|


|**Die diagram, nachdem die Form bearbeitet wurde**|
|:- |
|![todo: Bild_alt_Text](working-with-text_4.png)|
Der Prozess zum Ändern des Textes der Form:

1. Laden Sie eine diagram.
1. Finden Sie einen bestimmten Text einer Form.
1. Text dieser Form ersetzen
1. Speichern Sie die diagram.
### **Programmierbeispiel zum Suchen und Ersetzen von Text**
Die folgenden Codeausschnitte zeigen, wie der Text der Form geändert werden kann. Der Code durchläuft die Shapes einer Seite.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.cs" >}}
## **Extrahieren Sie Klartext von der Seite Visio Diagram**
Aspose.Diagram API ermöglicht es Entwicklern, Klartext aus der Seite Visio diagram zu extrahieren. Sie können auch die Visio diagram-Seiten durchlaufen, um den gesamten Visio diagram-Text abzudecken.

 Microsoft Office Visio fügt den Text zu den Formen hinzu. Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse enthält ein Element namens Text, das die Zeichen des Textes und spezielle Elemente (cp, pp, tp und fld) enthält, die das Ende eines Laufs und den Beginn des nächsten markieren.
### **Extrahieren Sie ein Klartext-Programmierbeispiel**
Der folgende Codeabschnitt durchläuft die Formen der Seite Visio und filtert einfachen Text ohne Formatierungsinformationen.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.cs" >}}
