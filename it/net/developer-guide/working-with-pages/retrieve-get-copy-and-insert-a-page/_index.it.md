---
title: Recupera, ottieni, copia e inserisci una pagina
type: docs
weight: 10
url: /it/net/retrieve-get-copy-and-insert-a-page/
description: Questa sezione spiega come inserire una pagina, copiare una pagina o ottenere informazioni sulla pagina con Aspose.Diagram.
---
## **Recupero delle informazioni sulla pagina**
In Microsoft Visio, le pagine sono in primo piano o in secondo piano. Per ottenere informazioni sulla pagina, ad esempio l'ID della pagina e il nome della pagina, stabilire innanzitutto se una pagina è una pagina di sfondo o in primo piano.

 Il[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page)oggetto rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta da[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supporta una raccolta di oggetti Aspose.Diagram.Page. Questa proprietà può essere utilizzata per recuperare informazioni sulla pagina.

Utilizzare la proprietà Page.Background per determinare se una pagina è in primo piano o in background.
### **Recupera il campione di programmazione delle informazioni sulla pagina**
Il seguente pezzo di codice recupera le informazioni sulle pagine da un diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}

## **Ottieni la pagina Visio da uno Diagram**
A volte, gli sviluppatori devono ottenere i dettagli della pagina di un disegno Visio. Aspose.Diagram ha caratteristiche che li aiutano a farlo.

 Aspose.Diagram for .NET offre il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio. La proprietà Pages esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Page. La classe PageCollection espone il metodo GetPage che può essere chiamato per ottenere l'oggetto Page.
### **Ottenere un oggetto pagina Visio per ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.

L'esempio seguente mostra come ottenere un oggetto pagina in base all'ID dal disegno Visio.
#### **Esempio di programmazione Ottieni oggetto pagina per ID**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}

### **Ottenere un oggetto pagina Visio per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.
#### **Esempio di programmazione Ottieni oggetto pagina per nome**
L'esempio seguente mostra come ottenere un oggetto pagina per nome dal disegno Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}

## **Copia una pagina Visio in un'altra Diagram**
Aspose.Diagram for .NET API consente agli sviluppatori di copiare e aggiungere il proprio contenuto da uno Visio diagram a un altro. Questo argomento della guida spiega come eseguire questa attività.

 Aspose.Diagram for .NET API ha il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio. La proprietà Pages esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Page. La classe PageCollection espone il metodo Add che può essere chiamato per aggiungere un altro oggetto Page.

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Copia Visio Page in un'altra istanza di Page**
Il metodo Copy della classe Page accetta un'istanza di pagina da clonare.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Inserisci una pagina vuota in un disegno Visio**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) può inserire una nuova pagina vuota nel disegno Microsoft Office Visio. Questo argomento di esempio descrive come farlo.

Il metodo Add, esposto dalla raccolta Pages, consente agli sviluppatori di aggiungere una nuova pagina vuota in Visio diagram. L'ID pagina deve essere assegnato.
### **Inserisci un esempio di programmazione in una pagina vuota**
La seguente parte di codice inserisce una pagina vuota nel disegno Visio:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Sposta la posizione della pagina nel disegno Visio**
Aspose.Diagram for .NET API può spostare la posizione della pagina nel disegno Visio. Il metodo MoveTo, esposto dalla classe Page, aiuta gli sviluppatori a spostare la posizione della pagina.
### **Sposta Posizione pagina Esempio di programmazione**
Il membro MoveTo utilizza l'indice della pagina di destinazione come parametro per spostare la posizione della pagina nel disegno Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
