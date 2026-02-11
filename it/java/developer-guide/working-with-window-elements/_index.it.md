---
title: Lavorare con gli elementi della finestra
type: docs
weight: 130
url: /it/java/working-with-window-elements/
---
## **Recupera gli elementi della finestra dal disegno Visio**
 La finestra principale dell'applicazione Visio può contenere qualsiasi file Visio aperto, allo stesso modo in cui i moderni browser Web consentono più pagine Web a schede in una finestra. Gli sviluppatori possono recuperare oggetti Window utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 Il[WindowCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) oggetto rappresenta un elenco di[Finestra](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)oggetti disponibili nel disegno. La proprietà Windows, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Window. Questa proprietà può essere utilizzata per recuperare le informazioni sulla finestra, ovvero l'ID della finestra, il tipo, l'altezza, la larghezza e lo stato.

**Una finestra della console che mostra l'output del codice.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/zduARGh.png)
### **Recupera l'esempio di programmazione degli elementi della finestra**
```
{{< highlight "java" >}}
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
```
## **Aggiungi elemento finestra a Visio Diagram**
 La finestra principale dell'applicazione Visio può contenere qualsiasi file Visio aperto, allo stesso modo in cui i moderni browser Web consentono più pagine Web a schede in una finestra. Gli sviluppatori possono ora aggiungere un nuovo oggetto Window in un'istanza Microsoft Visio utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

L'oggetto Window rappresenta una finestra aperta in un'istanza Microsoft Visio. Il metodo Add, esposto dalla classe WindowCollection, permette di aggiungere un nuovo oggetto Window.
### **Aggiungi esempio di programmazione di elementi finestra**
```
{{< highlight "java" >}}
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
```
## **Aggiungere il supporto di griglie dinamiche e punti di connessione**
La griglia dinamica ti aiuta a posizionare nuove forme verticalmente e orizzontalmente rispetto alle forme che hai già inserito nel disegno. Per quanto riguarda i punti di connessione, una volta contrassegnati come selezionati, ci aiuterà a vedere i punti di connessione quando siamo in procinto di connetterci ad essi. Possiamo ottenere entrambe le opzioni utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Supporto di griglie dinamiche e punti di connessione nei disegni Visio**
La classe Window offre le proprietà DynamicGridEnabled e ShowConnectionPoints. Queste proprietà possono essere utilizzate per applicare le impostazioni per supportare le griglie dinamiche e mostrare le opzioni dei punti di connessione.

**Un'applicazione Visio che mostra le opzioni in Visio.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/bxsJIwF.png)
#### **Aggiungi un esempio di programmazione di supporto**
```
{{< highlight "java" >}}
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
```
## **Mostra e nascondi griglie, righelli, guide e interruzioni di pagina del Visio Diagram**
 Microsoft Office Visio ha un paio di righelli, una griglia e due tipi di guide e flag di interruzioni di pagina per vedere cosa verrà stampato su ogni pagina. Gli sviluppatori possono applicare queste impostazioni utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)Le impostazioni si applicano globalmente a una singola pagina.

La classe Window offre proprietà ShowGrid, ShowGuides, ShowRulers e ShowPageBreaks. Queste proprietà possono essere utilizzate per applicare impostazioni per mostrare e nascondere griglie, guide, righelli e interruzioni di pagina.

**Un'applicazione Visio che mostra le opzioni in Visio.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/E0pvXbP.png)
### **Esempio di programmazione**
```
{{< highlight "java" >}}
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
```
