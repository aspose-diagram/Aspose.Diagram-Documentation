---
title: Recupera, ottieni, copia e inserisci una pagina
type: docs
weight: 10
url: /it/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Recupero delle informazioni sulla pagina**
In Microsoft Visio, le pagine sono in primo piano o in secondo piano. Per ottenere informazioni sulla pagina, ad esempio l'ID della pagina e il nome della pagina, stabilire innanzitutto se una pagina è una pagina di sfondo o in primo piano.

L'oggetto `Page` rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta dalla classe `Diagram` supporta una raccolta di oggetti Page. Questa proprietà può essere utilizzata per recuperare informazioni sulla pagina.

Utilizzare la proprietà `Page.Background` per determinare se una pagina è in primo piano o in background.

### **Recupera il campione di programmazione delle informazioni sulla pagina**
Il seguente pezzo di codice recupera le informazioni sulle pagine da un diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-RetrievePageInfo.py" >}}

## **Ottieni la pagina Visio da uno Diagram**
A volte, gli sviluppatori devono ottenere i dettagli della pagina di un disegno Visio. Aspose.Diagram per Python tramite Java ha caratteristiche che li aiutano a farlo.

Aspose.Diagram per Python tramite Java offre la classe `Diagram` che rappresenta un disegno Visio. La proprietà Pages esposta dalla classe Diagram supporta una raccolta di oggetti `Page`. La classe PageCollection espone il metodo `getPage` che può essere chiamato per ottenere l'oggetto Page.

### **Ottenere un oggetto pagina Visio per ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo getPage della classe Diagram.Pages.

L'esempio seguente mostra come ottenere un oggetto pagina in base all'ID dal disegno Visio.

#### **Esempio di programmazione Ottieni oggetto pagina per ID**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyID.py" >}}

### **Ottenere un oggetto pagina Visio per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetPage della classe Diagram.Pages.

#### **Esempio di programmazione Ottieni oggetto pagina per nome**
L'esempio seguente mostra come ottenere un oggetto pagina per nome dal disegno Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyName.py" >}}

## **Copia una pagina Visio in un'altra Diagram**
Aspose.Diagram per Python tramite Java API consente agli sviluppatori di copiare e aggiungere il proprio contenuto da uno Visio diagram a un altro. Questo argomento della guida spiega come eseguire questa operazione.

Aspose.Diagram per Python tramite Java API ha la classe `Diagram` che rappresenta un disegno Visio. La proprietà Pages esposta dalla classe Diagram supporta una raccolta di oggetti `Page`. La classe PageCollection espone il metodo `add` che può essere chiamato per aggiungere un altro oggetto Page.

Questo esempio funziona come segue:

1. Crea un nuovo oggetto della classe Diagram.
1. Carica un Visio diagram esistente nell'oggetto classe Diagram.
1. Aggiungi tutti i master dal Visio diagram caricato
1. Ottieni l'oggetto della pagina dallo diagram caricato (che deve essere copiato).
1. Imposta il nome e l'id dell'oggetto della pagina.
1. Rimuovere la pagina vuota del nuovo diagram (facoltativo).
1. Chiama il metodo add della classe PageCollection.
1. Salvare il nuovo diagram nella memoria del computer.

### **Copia un esempio di programmazione della pagina Visio**
L'esempio di codice seguente mostra come copiare un oggetto pagina Visio in un altro disegno Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-CopyVisioPage.py" >}}

## **Copia Visio Page in un'altra istanza di Page**
Il metodo `copy` della classe `Page` accetta un'istanza di pagina da clonare.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Inserisci una pagina vuota in un disegno Visio**
Aspose.Diagram per Python tramite Java può inserire una nuova pagina vuota nel disegno Microsoft Office Visio. Questo argomento di esempio descrive come farlo.

Il metodo `add`, esposto dalla raccolta Pages, consente agli sviluppatori di aggiungere una nuova pagina vuota in Visio diagram. L'ID pagina deve essere assegnato.

### **Inserisci un esempio di programmazione in una pagina vuota**
La seguente parte di codice inserisce una pagina vuota nel disegno Visio:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-InsertBlankPageInVisio.py" >}}

## **Sposta la posizione della pagina nel disegno Visio**
Aspose.Diagram per Python tramite Java API può spostare la posizione della pagina nel disegno Visio. Il metodo `moveTo`, esposto dalla classe `Page`, aiuta gli sviluppatori a spostare la posizione della pagina.

### **Sposta Posizione pagina Esempio di programmazione**
Il membro MoveTo utilizza l'indice della pagina di destinazione come parametro per spostare la posizione della pagina nel disegno Visio:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
