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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-RetrievePageInfo-RetrievePageInfo.cs" >}}
## **Ottieni la pagina Visio da uno Diagram**
A volte, gli sviluppatori devono ottenere i dettagli della pagina di un disegno Visio. Aspose.Diagram ha caratteristiche che li aiutano a farlo.

 Aspose.Diagram for .NET offre il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio. La proprietà Pages esposta dalla classe Diagram supporta una raccolta di oggetti Aspose.Diagram.Page. La classe PageCollection espone il metodo GetPage che può essere chiamato per ottenere l'oggetto Page.
### **Ottenere un oggetto pagina Visio per ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.

L'esempio seguente mostra come ottenere un oggetto pagina in base all'ID dal disegno Visio.
#### **Esempio di programmazione Ottieni oggetto pagina per ID**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyID-GetVisioPagebyID.cs" >}}
### **Ottenere un oggetto pagina Visio per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.
#### **Esempio di programmazione Ottieni oggetto pagina per nome**
L'esempio seguente mostra come ottenere un oggetto pagina per nome dal disegno Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyName-GetVisioPagebyName.cs" >}}
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-CopyVisioPage-CopyVisioPage.cs" >}}
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.cs" >}}
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
