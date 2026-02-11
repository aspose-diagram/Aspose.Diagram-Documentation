---
title: Recupera, ottieni, copia e inserisci una pagina
type: docs
weight: 10
url: /it/java/retrieve-get-copy-and-insert-a-page/
---
## **Recupero delle informazioni sulla pagina**
In Microsoft Visio, le pagine sono in primo piano o in secondo piano. Per ottenere informazioni sulla pagina, ad esempio l'ID della pagina e il nome della pagina, stabilire innanzitutto se una pagina è una pagina di sfondo o in primo piano.

 Il[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)oggetto rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta da[Diagram](https://reference.aspose.com/diagram/java) class supporta una raccolta di oggetti Aspose.Diagram.Page. Questa proprietà può essere utilizzata per recuperare informazioni sulla pagina.

Utilizzare la proprietà Page.Background per determinare se una pagina è in primo piano o in background.

L'immagine seguente mostra l'output dei frammenti di codice in questo articolo.

**Una console che mostra l'output.** 

![cose da fare:immagine_alt_testo](retrieve-get-copy-and-insert-a-page_1.png)
### **Recupera il campione di programmazione delle informazioni sulla pagina**
Il seguente pezzo di codice recupera le informazioni sulle pagine da un diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrievePageInfo.class);

//Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrievePageInfo.vdx");

for (Page page : (Iterable<Page>) diagram.getPages())
{
    //Checks if current page is a background page
    if (page.getBackground() == com.aspose.diagram.BOOL.TRUE)
    {
        //Display information about the background page
        System.out.println("Background Page ID : " + page.getID());
        System.out.println("Background Page Name : " + page.getName());
    }
    else
    {
        //Display information about the foreground page
        System.out.println("\nPage ID : " + page.getID());
        System.out.println("Universal Name : " + page.getNameU());
        System.out.println("ID of the Background Page : " + page.getBackPage());
    }
}

{{< /highlight >}}

## **Ottieni la pagina Visio da uno Diagram**
A volte, gli sviluppatori devono ottenere i dettagli della pagina di un disegno Visio. Aspose.Diagram ha caratteristiche che li aiutano a farlo.

 Aspose.Diagram for Java offre il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class che rappresenta un disegno Visio. La proprietà Pages esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Page. La classe PageCollection espone il metodo GetPage che può essere chiamato per ottenere l'oggetto Page.
### **Ottenere un oggetto pagina Visio per ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.

L'esempio seguente mostra come ottenere un oggetto pagina in base all'ID dal disegno Visio.
#### **Esempio di programmazione Ottieni oggetto pagina per ID**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyID.class); 
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.getPages().getPage(pageid);

{{< /highlight >}}

### **Ottenere un oggetto pagina Visio per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.
#### **Esempio di programmazione Ottieni oggetto pagina per nome**
L'esempio seguente mostra come ottenere un oggetto pagina per nome dal disegno Visio.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyName.class);     
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
String pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.getPages().getPage(pageName);

{{< /highlight >}}

## **Copia una pagina Visio in un'altra Diagram**
Aspose.Diagram for Java API consente agli sviluppatori di copiare e aggiungere il proprio contenuto da uno Visio diagram a un altro. Questo argomento della guida spiega come eseguire questa attività.

 Aspose.Diagram for Java API ha il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class che rappresenta un disegno Visio. La proprietà Pages esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Page. La classe PageCollection espone il metodo Add che può essere chiamato per aggiungere un altro oggetto Page.

Questo esempio funziona come segue:

1. Crea un nuovo oggetto della classe Diagram.
1. Carica un Visio diagram esistente nell'oggetto classe Diagram.
1. Aggiungi tutti i master dal Visio diagram caricato
1. Ottieni l'oggetto della pagina dallo diagram caricato (che deve essere copiato).
1. Imposta il nome e l'id dell'oggetto della pagina.
1. Rimuovere la pagina vuota del nuovo diagram (facoltativo).
1. Chiamare il metodo Add della classe PageCollection.
1. Salvare il nuovo diagram nella memoria del computer.
### **Copia un esempio di programmazione della pagina Visio**
L'esempio di codice seguente mostra come copiare un oggetto pagina Visio in un altro disegno Visio.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyVisioPage.class);
        
// Call the diagram constructor to load diagram from a VSD file
Diagram originalDiagram = new Diagram(dataDir + "Drawing1.vsd");

// initialize the new visio diagram
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = originalDiagram.getMasters();
for (Master master : (Iterable<Master>) originalMasters) {
   newDiagram.addMaster(originalDiagram, master.getName());
}

// get the page object from the original diagram
Page SrcPage = originalDiagram.getPages().getPage("Page-1");
// set page name
SrcPage.setName("new page");
        
// it calculates max page id
int max = 0;
if (newDiagram.getPages().getCount() != 0)
    max = newDiagram.getPages().get(0).getID();

for (int i = 1; i < newDiagram.getPages().getCount(); i++)
{
    if (max < newDiagram.getPages().get(i).getID())
        max = newDiagram.getPages().get(i).getID();
}
       
int MaxPageId = max;
// set page id
SrcPage.setID(MaxPageId);
// add reference of the original diagram page
newDiagram.getPages().add(SrcPage);

// remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0));

// save diagram in VDX format
newDiagram.save(dataDir + "CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Copia Visio Page in un'altra istanza di Page**
Il metodo Copy della classe Page accetta un'istanza di pagina da clonare.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Inserisci una pagina vuota in un disegno Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) può inserire una nuova pagina vuota nel disegno Microsoft Office Visio. Questo argomento di esempio descrive come farlo.

Il metodo Add, esposto dalla raccolta Pages, consente agli sviluppatori di aggiungere una nuova pagina vuota in Visio diagram. L'ID pagina deve essere assegnato.
### **Inserisci un esempio di programmazione in una pagina vuota**
La seguente parte di codice inserisce una pagina vuota nel disegno Visio:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(InsertBlankPageInVisio.class);   
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// it calculates max page id
int max = 0;
if (diagram.getPages().getCount() != 0)
    max = diagram.getPages().get(0).getID();

for (int i = 1; i < diagram.getPages().getCount(); i++)
{
    if (max < diagram.getPages().get(i).getID())
        max = diagram.getPages().get(i).getID();
}
        
// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.setName("new page");
// Set page ID
newPage.setID(max + 1);

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.getPages().add(newPage);

// Save diagram
diagram.save(dataDir + "InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Sposta la posizione della pagina nel disegno Visio**
Aspose.Diagram for Java API può spostare la posizione della pagina nel disegno Visio. Il metodo moveTo, esposto dalla classe Page, aiuta gli sviluppatori a spostare la posizione della pagina.
### **Sposta Posizione pagina Esempio di programmazione**
Il membro MoveTo utilizza l'indice della pagina di destinazione come parametro per spostare la posizione della pagina nel disegno Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
