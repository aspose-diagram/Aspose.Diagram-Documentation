---
title: Legen Sie die XForm-, Linien- und Fülldaten von Visio Form fest
type: docs
weight: 20
url: /de/net/set-visio-shape-s-xform-line-and-fill-data/
description: In diesem Abschnitt wird erläutert, wie Sie den Stil der Form festlegen, einschließlich der Liniendaten und Fülldaten mit Aspose.Diagram.
---
## **Festlegen von XForm-Daten**
 Das XForm-Element ist Teil des XML-Schemas Microsoft Visio. XForm gibt die Position einer Form an, z. B. Breite, Höhe, Drehung und ob die Form gespiegelt wurde. Das[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) Eigentum, ausgesetzt durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützt das Objekt Aspose.Diagram.XForm. Die XForm-Eigenschaft kann verwendet werden, um die XForm-Daten einer Form abzurufen oder zu aktualisieren. Die Codebeispiele in diesem Artikel ändern die XForm-Werte PinX (X-Koordinate) und PinY (Y-Koordinate), um die Shapes auf der Seite zu verschieben.

Der Prozess zum Aktualisieren von XForm-Daten ist:

1. Laden Sie ein diagram.# Finden Sie eine bestimmte Form.# Aktualisieren Sie die XForm-Daten der Form.
1. Speichern Sie die diagram.
### **Programmierbeispiel**
Das folgende Code-Snippet zeigt, wie die XForm-Daten einer Form aktualisiert werden. Der Code sucht nach einem Shape-Namensprozess mit der Shape-ID 1 und setzt seine X- und Y-Koordinaten auf 5.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **Legen Sie die Liniendaten der Form Visio fest**
Formen können auf verschiedene Arten formatiert werden. Dieser Artikel zeigt, wie Sie die Attribute einer Linie angeben.

Microsoft Visio lässt Benutzer Linien auf verschiedene Arten formatieren. Aspose.Diagram for .NET unterstützt:

- Gewicht: die Dicke einer Linie.
- Farbe: Legen Sie die Linienfarbe der Form fest.
- Transparenz der Linienfarbe: Legen Sie die Transparenz der Linienfarbe der Form in Prozent fest.
- Muster: legt fest, ob die Linie durchgezogen, gestrichelt oder mit einem anderen Muster ist.
- Rundung: der Radius der Ecken.
- Anfangs- und Endpfeile: Gibt an, ob die Linie Pfeile hat.
- Anfangs- und Endpfeilgröße: Legen Sie die Pfeilgröße fest.
- Kappe: die Rundung der Linienenden.
### **Ändern Sie die Linienfarbe, das Gewicht, den Strichtyp, die Transparenz, die Rundung, den Pfeiltyp und die Pfeilgröße des Rahmens einer Form**
 Das[Linie](http://www.aspose.com/api/net/diagram/aspose.diagram/line) Eigentum, ausgesetzt durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)Klasse, unterstützt das Objekt Aspose.Diagram.Line. Diese Eigenschaft kann verwendet werden, um die Liniendaten einer Form abzurufen oder zu aktualisieren.
#### **Programmierbeispiel für Leitungsdaten**
Der folgende Codeabschnitt aktualisiert die Liniendaten von shape.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **Legen Sie die Fülldaten der Form Visio fest**
 Formen können auf verschiedene Arten formatiert werden. In diesem Thema wird beschrieben, wie Sie die Füllung einer Form angeben. Microsoft Office Visio lässt Benutzer Füllungen auf verschiedene Weise formatieren. Das[Füllen](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) Klasse der Aspose.Diagram for .NET API unterstützt Einstellung:

- Hintergrund- und Vordergrundfarben.
- Transparenz.
- Muster füllen.
- Schatten.
### **Füllwerte einstellen**
 Die Fill-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützt die[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) Objekt. Die Fill-Eigenschaft kann verwendet werden, um die Fülldaten einer Form abzurufen oder zu aktualisieren.
#### **Füllen Sie das Programmierbeispiel für Daten aus**
Der folgende Codeausschnitt aktualisiert die Fülldaten einer Form. Der Code sucht nach einer Form namens Rechteck mit der Form-ID 1 und legt die Hintergrund- und Vordergrundfarben für die Füllung fest.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **Rufen Sie geerbte Fülldaten einer Visio-Form ab**
 Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die vererbten Fülldaten einer Visio-Form abrufen oder festlegen. Die InheritFill-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, enthält die Füllformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Fülldaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Fülldaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
