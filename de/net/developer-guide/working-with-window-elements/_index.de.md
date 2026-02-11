---
title: Arbeiten mit Fensterelementen
type: docs
weight: 100
url: /de/net/working-with-window-elements/
description: In diesem Abschnitt wird das Abrufen der Eigenschaft von Fensterelementen in visio mit Aspose.Diagram erläutert.
---
## **Abrufen von Fensterelementen aus der Zeichnung Visio**
 Das Hauptfenster der Visio-Anwendung kann alle geöffneten Visio-Dateien enthalten, genauso wie moderne Webbrowser Webseiten mit mehreren Registerkarten in einem Fenster zulassen. Entwickler können Windows-Objekte mit abrufen[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 Das[WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) Objekt repräsentiert eine Liste von[Fenster](http://www.aspose.com/api/net/diagram/aspose.diagram/window)in der Zeichnung verfügbare Objekte. Die Windows-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Window-Objekten. Diese Eigenschaft kann verwendet werden, um die Fensterinformationen abzurufen, d. h. Fenster-ID, Typ, Höhe, Breite und Status.
### **Programmierbeispiel für Fensterelemente abrufen**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Iterate through the window elements
foreach (Window window in diagram.Windows)
{
    Console.WriteLine("ID: " + window.ID);
    Console.WriteLine("Type: " + window.WindowType);
    Console.WriteLine("Window height: " + window.WindowHeight);
    Console.WriteLine("Window width: " + window.WindowWidth);
    Console.WriteLine("Window state: " + window.WindowState);
}

{{< /highlight >}}
```
## **Fensterelement zu Visio Diagram hinzufügen**
 Das Hauptfenster der Visio-Anwendung kann alle geöffneten Visio-Dateien enthalten, genauso wie moderne Webbrowser Webseiten mit mehreren Registerkarten in einem Fenster zulassen. Entwickler können jetzt ein neues Window-Objekt in einer Microsoft Visio-Instanz mit hinzufügen[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 Das[Fenster](http://www.aspose.com/api/net/diagram/aspose.diagram/window) Objekt repräsentiert ein offenes Fenster in einer Microsoft Visio Instanz. Das[Hinzufügen](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) Methode, ausgesetzt durch die[WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) Klasse, ermöglicht das Hinzufügen eines neuen Window-Objekts.
### **Programmierbeispiel für Fensterelemente hinzugefügt**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Initialize window object
Window window = new Window();
// Set window state
window.WindowState = WindowStateValue.Maximized;
// Set window height
window.WindowHeight = 500;
// Set window width
window.WindowWidth = 500;
// Set window type
window.WindowType = WindowTypeValue.Stencil;
// Add window object
diagram.Windows.Add(window);

// Save in any supported format
diagram.Save(dataDir + "AddWindowElementInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Unterstützung für dynamische Gitter und Verbindungspunkte hinzufügen**
Das dynamische Raster hilft Ihnen, neue Formen vertikal und horizontal relativ zu den Formen zu positionieren, die Sie bereits in der Zeichnung platziert haben. In Bezug auf die Verbindungspunkte, sobald sie als markiert markiert sind, hilft uns, die Verbindungspunkte zu sehen, wenn wir dabei sind, eine Verbindung zu ihnen herzustellen. Wir können beide Optionen mit erreichen[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Unterstützung dynamischer Gitter und Verbindungspunkte in den Visio-Zeichnungen**
 Das[Fenster](http://www.aspose.com/api/net/diagram/aspose.diagram/window) -Klasse bietet die Eigenschaften DynamicGridEnabled und ShowConnectionPoints. Diese Eigenschaften können verwendet werden, um Einstellungen anzuwenden, um dynamische Raster zu unterstützen und Optionen für Verbindungspunkte anzuzeigen.
#### **Support-Programmierbeispiel hinzufügen**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Check dynamic grid option
window.DynamicGridEnabled = BOOL.True;
// Check connection points option
window.ShowConnectionPoints = BOOL.True;
            
// Save visio drawing
diagram.Save(dataDir + "AddSupportOfVisualAids_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Raster, Lineale, Hilfslinien und Seitenumbrüche von Visio Diagram ein- und ausblenden**
 Microsoft Office Visio hat ein Linealpaar, ein Raster und zwei Arten von Hilfslinien und eine Seitenumbruchflagge, um zu sehen, was auf jeder Seite gedruckt wird. Entwickler können diese Einstellungen mit anwenden[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)Die Einstellungen gelten global für eine einzelne Seite.

 Das[Fenster](http://www.aspose.com/api/net/diagram/aspose.diagram/window)Die Klasse bietet die Eigenschaften ShowGrid, ShowGuides, ShowRulers und ShowPageBreaks. Diese Eigenschaften können verwendet werden, um Einstellungen zum Ein- und Ausblenden von Rastern, Hilfslinien, Linealen und Seitenumbrüchen anzuwenden.
### **Programmierbeispiel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Set visibility of grid
window.ShowGrid = BOOL.True;
// Set visibility of guides
window.ShowGuides = BOOL.True;
// Set visibility of rulers
window.ShowRulers = BOOL.True;
// Set visibility of page breaks
window.ShowPageBreaks = BOOL.True;

// Save diagram
diagram.Save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
