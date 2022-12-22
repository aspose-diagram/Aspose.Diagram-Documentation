---
title: Creare, aggiornare, disporre e adattare automaticamente le forme
type: docs
weight: 10
url: /it/net/create-update-layout-and-auto-fit-shapes/
description: Usa C# Diagram API per creare, aggiornare e creare forme di layout automatico nei file Visio utilizzando C# all'interno delle tue applicazioni. Guida completa con esempi di codice C#.
---
## **Creazione di un numero Diagram**
 Aspose.Diagram for .NET consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un numero diagram. Quindi[aggiungere forme e connettori](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)per creare diagram. Utilizzare il costruttore predefinito di[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class per creare un nuovo diagram.
### **Esempio di programmazione**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}
## **Forme di layout in stile diagramma di flusso**
 Con alcuni tipi di disegni collegati, come diagrammi di flusso e diagrammi di rete, è possibile utilizzare il file**Forme di layout** funzione per posizionare automaticamente le forme. Il posizionamento automatico è più rapido rispetto al trascinamento manuale di ciascuna forma in una nuova posizione.

Ad esempio, se stai aggiornando un diagramma di flusso di grandi dimensioni per includere un nuovo processo, puoi aggiungere e connettere le forme che compongono il processo e quindi utilizzare la funzionalità di layout per disporre automaticamente il disegno aggiornato.

 Il metodo Layout, esposto da[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class impagina le forme e/o reindirizza i connettori su tutte le pagine di diagram. Questo metodo accetta un file[LayoutOptions](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)oggetto come argomento. Usare le diverse proprietà esposte dalla classe LayoutOptions per disporre automaticamente le forme.

L'immagine seguente mostra lo diagram caricato dai frammenti di codice in questo articolo, prima che venga applicato il layout automatico. I frammenti di codice mostrano come fare domanda[layout del diagramma di flusso](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) e[layout ad albero compatto](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**La fonte diagram.**

![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_1.png)

I frammenti di codice in questo articolo prendono il codice sorgente diagram e vi applicano diversi tipi di layout automatico, salvandoli ciascuno in un file separato.

|<p>**Layout delle forme dal basso verso l'alto** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layout delle forme dall'alto verso il basso** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Forme di layout da sinistra a destra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layout delle forme da destra a sinistra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Per disporre le forme in stile diagramma di flusso:

1. Creare un'istanza della classe Diagram.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà correlate allo stile del diagramma di flusso.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il disegno Visio.
### **Esempio di programmazione in stile diagramma di flusso**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.cs" >}}
### **Disposizione delle forme nello stile ad albero compatto**
 Lo stile di layout ad albero compatto cerca di costruire una struttura ad albero. Utilizza lo stesso file di input del file[esempio sopra](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) salva in diversi stili di alberi compatti diversi.

|<p>**Layout ad albero compatto - in basso ea destra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Layout ad albero compatto - in basso ea sinistra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Layout ad albero compatto - a destra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Layout ad albero compatto - a sinistra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Per disporre le forme nello stile ad albero compatto:

1.  Crea un'istanza di[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà dello stile dell'albero compatto.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il file Visio.
#### **Esempio di programmazione in stile albero compatto**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.cs" >}}
## **Adatta automaticamente il Visio Diagram**
 Aspose.Diagram API supporta l'autoadattamento del disegno Visio. Questa operazione di funzionalità aiuta a portare le forme esterne all'interno del limite di pagina Visio. Aspose.Diagram for .NET API ha il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio. Il[DiagramSaveOptions](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) espone la proprietà AutoFitPageToDrawingContent per adattare automaticamente il disegno Visio.

Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Crea un oggetto della classe DiagramSaveOptions e passa il formato di file risultante.
1. Impostare la proprietà AutoFitPageToDrawingContent dell'oggetto DiagramSaveOptions.
1. Chiama il metodo Save dell'oggetto classe Diagram e passa anche il percorso file completo e l'oggetto DiagramSaveOptions.
### **Esempio di programmazione dell'adattamento automatico**
Il codice di esempio seguente mostra come adattare automaticamente le forme nel Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.cs" >}}
## **Lavorare con il progetto VBA**
### **Modifica il codice del modulo VBA in Visio Diagram**
 Questo articolo mostra come modificare automaticamente il codice di un modulo VBA utilizzando Aspose.Diagram for .NET. Abbiamo aggiunto[Modulo Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) e[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) classi. Queste classi aiutano a ottenere il controllo sul progetto VBA. Gli sviluppatori possono estrarre e modificare il codice del modulo VBA.
### **Modifica l'esempio di programmazione del codice del modulo VBA**
Si prega di controllare questo esempio di codice:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-ModifyVBAModule-ModifyVBAModule.cs" >}}
### **Rimuovi tutte le macro da Visio Diagram**
 Aspose.Diagram for .NET consente agli sviluppatori di rimuovere tutte le macro da Visio diagram. La proprietà VbProjectData, esposta dal[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, permette di rimuovere tutte le macro dal disegno Visio.
### **Esempio di programmazione Rimuovi tutte le macro**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.cs" >}}
## **Creazione di un nuovo Diagram con VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)consente agli sviluppatori di creare e lavorare con diagrammi Microsoft Office Visio e incorporare funzionalità nelle loro applicazioni software. Esistono altri modi per lavorare con i file Visio, più comunemente, Microsoft Automation. Sfortunatamente, questo ha alcune limitazioni. Aspose.Diagram è potente e veloce e funziona in modo indipendente senza Microsoft Office installazione.

 Questo articolo sulla migrazione mostra come utilizzare first[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) poi[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) per creare un nuovo diagram e aggiungervi alcune forme. Noterai che il codice Aspose.Diagram è più corto del codice VSTO. Sentiti libero di utilizzare il codice come base per il tuo sviluppo e di migliorarlo per soddisfare le tue esigenze. VSTO ti consente di programmare con file Microsoft Visio. Per creare un nuovo diagram:

1. Creare un oggetto applicazione Visio.
1. Rendi invisibile l'oggetto dell'applicazione.
1. Crea un diagram vuoto.
1. Aggiungi forme da Visio maestri (stencil).
1. Salva il file come VDX.
### **Crea nuovo Diagram con esempio di programmazione VSTO**
{{% alert color="primary" %}}

utilizzando Visio = Microsoft.Office.Interop.Visio;
Importazioni Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Esempio:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithVSTO-CreatingDiagramWithVSTO.cs" >}}
## **Creazione di un nuovo Diagram con Aspose.Diagram for .NET**
Utilizzando Aspose.Diagram API, gli sviluppatori non hanno bisogno dell'installazione Microsoft Office Visio sulla macchina e possono lavorare indipendentemente dall'automazione Microsoft Office.

Per creare un nuovo diagram:

1. Crea un diagram vuoto.
1. Aggiungi forme da Visio maestri (stencil).
1. Salva il file come VDX.
### **Nuovo Diagram con Aspose.Diagram for .NET Esempio di programmazione**
{{% alert color="primary" %}}

utilizzando il numero Aspose.Diagram;
Importazioni Aspose.Diagram

{{% /alert %}}

Esempio:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithAspose-CreatingDiagramWithAspose.cs" >}}
## **Aggiorna proprietà forma**
 Quando si lavora con i diagrammi Microsoft Visio, gli utenti possono aggiornare gli attributi della forma inclusi testo, stile, posizione, altezza e larghezza. Come sviluppatore di software che lavora con i file Visio, ti verrà chiesto di farlo a livello di codice. La buona notizia è che è possibile, sia utilizzando i meccanismi di programmazione con i file Visio forniti da Microsoft, VSTO, sia utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Sotto argomento mostra come utilizzare[VSTO](https://products.aspose.com/diagram/net/) e[Aspose.Diagram](https://products.aspose.com/diagram/net/) per aggiornare le proprietà della forma. I frammenti di codice seguenti mostrano come aggiornare le proprietà della forma per VSTO e Aspose.Diagram for .NET. Sentiti libero di usare il codice e applicarlo alla tua situazione particolare.
### **Aggiornamento delle proprietà della forma con VSTO**
VSTO ti consente di programmare con file Microsoft Visio. Per aggiornare le proprietà della forma:

1. Creare un oggetto applicazione Visio.
1. Rendi invisibile l'oggetto dell'applicazione.
1. Apri un file Visio VSD esistente.
1. Trova la forma richiesta.
1. Aggiorna le proprietà della forma (testo, stile del testo, posizione e dimensione).
1. Salva il file come VDX.
#### **Aggiornamento delle proprietà della forma con l'esempio di programmazione VSTO**
{{% alert color="primary" %}}

utilizzando Visio = Microsoft.Office.Interop.Visio;
Importazioni Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Esempio:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithVSTO-UpdateShapePropsWithVSTO.cs" >}}
### **Aggiornamento delle proprietà della forma con Aspose.Diagram for .NET**
Utilizzando Aspose.Diagram API, gli sviluppatori non hanno bisogno di Microsoft Office Visio sulla macchina e possono lavorare indipendentemente dall'automazione Microsoft Office.

Per aggiornare le proprietà della forma con Aspose.Diagram for .NET:

1. Apri un file Visio VSD esistente.
1. Trova la forma richiesta.
1. Aggiorna le proprietà della forma (testo, stile del testo, posizione e dimensione).
1. Salva il file come VDX.
#### **Aggiornamento delle proprietà della forma con l'esempio di programmazione Aspose.Diagram for .NET**
{{% alert color="primary" %}}

utilizzando il numero Aspose.Diagram;
Importazioni Aspose.Diagram

{{% /alert %}}

**Esempio:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithAspose-UpdateShapePropsWithAspose.cs" >}}
