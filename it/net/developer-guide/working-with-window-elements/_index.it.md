---
title: Lavorare con gli elementi della finestra
type: docs
weight: 100
url: /it/net/working-with-window-elements/
description: Questa sezione spiega come ottenere la proprietà degli elementi della finestra in visio con Aspose.Diagram.
---
## **Recupera gli elementi della finestra dal disegno Visio**
 La finestra principale dell'applicazione Visio può contenere qualsiasi file Visio aperto, allo stesso modo in cui i moderni browser Web consentono più pagine Web a schede in una finestra. Gli sviluppatori possono recuperare oggetti Window utilizzando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 Il[WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) oggetto rappresenta un elenco di[Finestra](http://www.aspose.com/api/net/diagram/aspose.diagram/window)oggetti disponibili nel disegno. La proprietà Windows, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Window. Questa proprietà può essere utilizzata per recuperare le informazioni sulla finestra, ovvero l'ID della finestra, il tipo, l'altezza, la larghezza e lo stato.
### **Recupera l'esempio di programmazione degli elementi della finestra**
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
## **Aggiungi elemento finestra a Visio Diagram**
 La finestra principale dell'applicazione Visio può contenere qualsiasi file Visio aperto, allo stesso modo in cui i moderni browser Web consentono più pagine Web a schede in una finestra. Gli sviluppatori possono ora aggiungere un nuovo oggetto Window in un'istanza Microsoft Visio utilizzando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 Il[Finestra](http://www.aspose.com/api/net/diagram/aspose.diagram/window) oggetto rappresenta una finestra aperta in un'istanza Microsoft Visio. Il[Aggiungere](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) metodo, esposto dal[WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) class, permette di aggiungere un nuovo oggetto Window.
### **Aggiungi esempio di programmazione di elementi finestra**
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
## **Aggiungere il supporto di griglie dinamiche e punti di connessione**
La griglia dinamica ti aiuta a posizionare nuove forme verticalmente e orizzontalmente rispetto alle forme che hai già inserito nel disegno. Per quanto riguarda i punti di connessione, una volta contrassegnati come selezionati, ci aiuterà a vedere i punti di connessione quando siamo in procinto di connetterci ad essi. Possiamo ottenere entrambe le opzioni utilizzando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Supporto di griglie dinamiche e punti di connessione nei disegni Visio**
 Il[Finestra](http://www.aspose.com/api/net/diagram/aspose.diagram/window) offre le proprietà DynamicGridEnabled e ShowConnectionPoints. Queste proprietà possono essere utilizzate per applicare le impostazioni per supportare le griglie dinamiche e mostrare le opzioni dei punti di connessione.
#### **Aggiungi un esempio di programmazione di supporto**
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
## **Mostra e nascondi griglie, righelli, guide e interruzioni di pagina del Visio Diagram**
 Microsoft Office Visio ha un paio di righelli, una griglia e due tipi di guide e flag di interruzioni di pagina per vedere cosa verrà stampato su ogni pagina. Gli sviluppatori possono applicare queste impostazioni utilizzando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)Le impostazioni si applicano globalmente a una singola pagina.

 Il[Finestra](http://www.aspose.com/api/net/diagram/aspose.diagram/window)offre le proprietà ShowGrid, ShowGuides, ShowRulers e ShowPageBreaks. Queste proprietà possono essere utilizzate per applicare impostazioni per mostrare e nascondere griglie, guide, righelli e interruzioni di pagina.
### **Esempio di programmazione**
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
