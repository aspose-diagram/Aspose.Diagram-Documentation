---
title: Arbeiten mit Fensterelementen
type: docs
weight: 130
url: /de/java/working-with-window-elements/
---
## **Abrufen von Fensterelementen aus der Zeichnung Visio**
 Das Hauptfenster der Visio-Anwendung kann alle geöffneten Visio-Dateien enthalten, genauso wie moderne Webbrowser Webseiten mit mehreren Registerkarten in einem Fenster zulassen. Entwickler können Windows-Objekte mit abrufen[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 Das[WindowCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) Objekt repräsentiert eine Liste von[Fenster](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)in der Zeichnung verfügbare Objekte. Die Windows-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Window-Objekten. Diese Eigenschaft kann verwendet werden, um die Fensterinformationen abzurufen, d. h. Fenster-ID, Typ, Höhe, Breite und Status.

**Ein Konsolenfenster, das die Ausgabe des Codes anzeigt.**

![todo: Bild_alt_Text](http://i.imgur.com/zduARGh.png)
### **Programmierbeispiel für Fensterelemente abrufen**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveWindowElementsOfDiagram.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// iterate through the window elements
for (Window window :(Iterable<Window>) diagram.getWindows())
{
    System.out.println("ID: " + window.getID());
    System.out.println("Type: " + window.getWindowType());
    System.out.println("Window height: " + window.getWindowHeight());
    System.out.println("Window width: " + window.getWindowWidth());
    System.out.println("Window state: " + window.getWindowState());
}

{{< /highlight >}}

## **Fensterelement zu Visio Diagram hinzufügen**
 Das Hauptfenster der Visio-Anwendung kann alle geöffneten Visio-Dateien enthalten, genauso wie moderne Webbrowser Webseiten mit mehreren Registerkarten in einem Fenster zulassen. Entwickler können jetzt ein neues Window-Objekt in einer Microsoft Visio-Instanz mit hinzufügen[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

Das Window-Objekt repräsentiert ein offenes Fenster in einer Microsoft Visio-Instanz. Die Add-Methode, die von der WindowCollection-Klasse verfügbar gemacht wird, ermöglicht das Hinzufügen eines neuen Window-Objekts.
### **Programmierbeispiel für Fensterelemente hinzugefügt**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWindowElementInVisio.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// initialize window object
Window window = new Window();
// set window state
window.setWindowState(WindowStateValue.MAXIMIZED);
// set window height
window.setWindowHeight(500);
// set window width
window.setWindowWidth(500);
// set window type
window.setWindowType(WindowTypeValue.STENCIL);
// add window object
diagram.getWindows().add(window);

// save in any supported format
diagram.save(dataDir + "AddWindowElementInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Unterstützung für dynamische Gitter und Verbindungspunkte hinzufügen**
Das dynamische Raster hilft Ihnen, neue Formen vertikal und horizontal relativ zu den Formen zu positionieren, die Sie bereits in der Zeichnung platziert haben. In Bezug auf die Verbindungspunkte, sobald sie als markiert markiert sind, hilft uns, die Verbindungspunkte zu sehen, wenn wir dabei sind, eine Verbindung zu ihnen herzustellen. Wir können beide Optionen mit erreichen[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Unterstützung dynamischer Gitter und Verbindungspunkte in den Visio-Zeichnungen**
Die Window-Klasse bietet die Eigenschaften DynamicGridEnabled und ShowConnectionPoints. Diese Eigenschaften können verwendet werden, um Einstellungen anzuwenden, um dynamische Raster zu unterstützen und Optionen für Verbindungspunkte anzuzeigen.

**Eine Visio-Anwendung, die die Optionen in Visio zeigt.**

![todo: Bild_alt_Text](http://i.imgur.com/bxsJIwF.png)
#### **Support-Programmierbeispiel hinzufügen**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSupportOfVisualAids.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// check dynamic grid option
window.setDynamicGridEnabled(BOOL.TRUE);
// check connection points option
window.setShowConnectionPoints(BOOL.TRUE);
        
// save visio drawing
diagram.save(dataDir + "AddSupportOfVisualAids_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Raster, Lineale, Hilfslinien und Seitenumbrüche von Visio Diagram ein- und ausblenden**
 Microsoft Office Visio hat ein Linealpaar, ein Raster und zwei Arten von Hilfslinien und eine Seitenumbruchflagge, um zu sehen, was auf jeder Seite gedruckt wird. Entwickler können diese Einstellungen mit anwenden[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)Die Einstellungen gelten global für eine einzelne Seite.

Die Window-Klasse bietet die Eigenschaften ShowGrid, ShowGuides, ShowRulers und ShowPageBreaks. Diese Eigenschaften können verwendet werden, um Einstellungen zum Ein- und Ausblenden von Rastern, Hilfslinien, Linealen und Seitenumbrüchen anzuwenden.

**Eine Visio-Anwendung, die die Optionen in Visio zeigt.**

![todo: Bild_alt_Text](http://i.imgur.com/E0pvXbP.png)
### **Programmierbeispiel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DisplayGridsRulersGuidesAndPageBreaks.class);     
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// set visibility of grid
window.setShowGrid(BOOL.TRUE);
// set visibility of guides
window.setShowGuides(BOOL.TRUE);
// set visibility of rulers
window.setShowRulers(BOOL.TRUE);
// set visibility of page breaks
window.setShowPageBreaks(BOOL.TRUE);

// save diagram
diagram.save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

