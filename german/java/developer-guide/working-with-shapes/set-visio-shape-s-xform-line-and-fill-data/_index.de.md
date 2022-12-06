---
title: Legen Sie die XForm-, Linien- und Fülldaten von Visio Form fest
type: docs
weight: 70
url: /de/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Festlegen von XForm-Daten**
 Das XForm-Element ist Teil des XML-Schemas Microsoft Visio. XForm gibt die Position einer Form an, z. B. Breite, Höhe, Drehung und ob die Form gespiegelt wurde. Das[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) Eigentum, ausgesetzt durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse, unterstützt das Objekt Aspose.Diagram.XForm. Die XForm-Eigenschaft kann verwendet werden, um die XForm-Daten einer Form abzurufen oder zu aktualisieren. Die Codebeispiele in diesem Artikel ändern die XForm-Werte PinX (X-Koordinate) und PinY (Y-Koordinate), um die Shapes auf der Seite zu verschieben.

**Geben Sie diagram ein** 

![todo: Bild_alt_Text](set-visio-shape-s-xform-line-and-fill-data_1.png)

**Die diagram nach der** **PinX** **und** **PinY** **Werte wurden geändert** 

![todo: Bild_alt_Text](set-visio-shape-s-xform-line-and-fill-data_2.png)

Der Prozess zum Aktualisieren von XForm-Daten ist:

1. Laden Sie ein diagram.# Finden Sie eine bestimmte Form.# Aktualisieren Sie die XForm-Daten der Form.
1. Speichern Sie die diagram.
### **Programmierbeispiel**
Das folgende Code-Snippet zeigt, wie die XForm-Daten einer Form aktualisiert werden. Der Code sucht nach einem Shape-Namensprozess mit der Shape-ID 1 und setzt seine X- und Y-Koordinaten auf 5.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetXFormdata-SetXFormdata.java" >}}
## **Legen Sie die Liniendaten der Form Visio fest**
Formen können auf verschiedene Arten formatiert werden. Dieser Artikel zeigt, wie Sie die Attribute einer Linie angeben.

Microsoft Visio lässt Benutzer Linien auf verschiedene Arten formatieren. Aspose.Diagram for Java unterstützt:

- Gewicht: die Dicke einer Linie.
- Farbe: Legen Sie die Linienfarbe der Form fest.
- Transparenz der Linienfarbe: Legen Sie die Transparenz der Linienfarbe der Form in Prozent fest.
- Muster: legt fest, ob die Linie durchgezogen, gestrichelt oder mit einem anderen Muster ist.
- Rundung: der Radius der Ecken.
- Anfangs- und Endpfeile: Gibt an, ob die Linie Pfeile hat.
- Anfangs- und Endpfeilgröße: Legen Sie die Pfeilgröße fest.
- Kappe: die Rundung der Linienenden.
### **Ändern Sie die Linienfarbe, das Gewicht, den Strichtyp, die Transparenz, die Rundung, den Pfeiltyp und die Pfeilgröße des Rahmens einer Form**
 Das[Linie](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) Eigentum, ausgesetzt durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)Klasse, unterstützt das Objekt Aspose.Diagram.Line. Diese Eigenschaft kann verwendet werden, um die Liniendaten einer Form abzurufen oder zu aktualisieren.
#### **Programmierbeispiel für Leitungsdaten**
Der folgende Codeabschnitt aktualisiert die Liniendaten von shape.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetLineData-SetLineData.java" >}}
## **Legen Sie die Fülldaten der Form Visio fest**
Formen können auf verschiedene Arten formatiert werden. In diesem Thema wird beschrieben, wie Sie die Füllung einer Form angeben.

 Microsoft Office Visio lässt Benutzer Füllungen auf verschiedene Weise formatieren. Das[Füllen](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) Klasse der Aspose.Diagram for Java API unterstützt Einstellung:

- Hintergrund- und Vordergrundfarben.
- Transparenz.
- Muster füllen.
- Schatten.
### **Füllwerte einstellen**
Die Fill-Eigenschaft, die von der Shape-Klasse verfügbar gemacht wird, unterstützt das Aspose.Diagram.Fill-Objekt. Die Fill-Eigenschaft kann verwendet werden, um die Fülldaten einer Form abzurufen oder zu aktualisieren.

|<p>**Die Eingabe diagram** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/OrhEecb.png)</p>|<p>**Die diagram nach dem Ändern der Füllfarbe** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Füllen Sie das Programmierbeispiel für Daten aus**
Der folgende Codeausschnitt aktualisiert die Fülldaten einer Form. Der Code sucht nach einer Form namens Rechteck mit der Form-ID 1 und legt die Hintergrund- und Vordergrundfarben für die Füllung fest.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetFillData-SetFillData.java" >}}
### **Rufen Sie geerbte Fülldaten einer Visio-Form ab**
Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die vererbten Fülldaten einer Visio-Form abrufen oder festlegen. Die InheritFill-Eigenschaft, die von der Shape-Klasse verfügbar gemacht wird, enthält die Füllungsformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt werden.
#### **Programmierbeispiel für geerbte Fülldaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Fülldaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveInheritedFillData-RetrieveInheritedFillData.java" >}}
