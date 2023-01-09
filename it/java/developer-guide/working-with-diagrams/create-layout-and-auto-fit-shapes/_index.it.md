---
title: Creazione, layout e adattamento automatico delle forme
type: docs
weight: 10
url: /it/java/create-layout-and-auto-fit-shapes/
---
## **Creazione di un numero Diagram**
 Aspose.Diagram for Java consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un numero diagram. Quindi[aggiungere forme e connettori](/diagram/it/java/add-and-connect-visio-shapes/)per creare diagram. Utilizzare il costruttore predefinito di[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class per creare un nuovo diagram.
### **Esempio di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-CreateDiagram-CreateDiagram.java" >}}
## **Forme di layout in stile diagramma di flusso**
 Con alcuni tipi di disegni collegati, come diagrammi di flusso e diagrammi di rete, è possibile utilizzare il file**Forme di layout** funzione per posizionare automaticamente le forme. Il posizionamento automatico è più rapido rispetto al trascinamento manuale di ciascuna forma in una nuova posizione.

Ad esempio, se stai aggiornando un diagramma di flusso di grandi dimensioni per includere un nuovo processo, puoi aggiungere e connettere le forme che compongono il processo e quindi utilizzare la funzionalità di layout per disporre automaticamente il disegno aggiornato.

 Il metodo Layout, esposto da[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class impagina le forme e/o reindirizza i connettori su tutte le pagine di diagram. Questo metodo accetta un oggetto LayoutOptions come argomento. Usare le diverse proprietà esposte dalla classe LayoutOptions per disporre automaticamente le forme.

L'immagine seguente mostra lo diagram caricato dai frammenti di codice in questo articolo, prima che venga applicato il layout automatico. I frammenti di codice mostrano come fare domanda[layout del diagramma di flusso](/diagram/it/java/create-2c-layout-and-auto-fit-shapes/) e[layout ad albero compatto](/diagram/it/java/create-2c-layout-and-auto-fit-shapes/).

**La fonte diagram.** 

![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_1.png)

I frammenti di codice in questo articolo prendono il codice sorgente diagram e vi applicano diversi tipi di layout automatico, salvandoli ciascuno in un file separato.

|<p>**Layout delle forme dal basso verso l'alto** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layout delle forme dall'alto verso il basso** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Forme di layout da sinistra a destra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layout delle forme da destra a sinistra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_5.png)</p>|
Per disporre le forme in stile diagramma di flusso:

1. Creare un'istanza della classe Diagram.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà correlate allo stile del diagramma di flusso.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il disegno Visio.
### **Esempio di programmazione in stile diagramma di flusso**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.java" >}}
### **Disposizione delle forme nello stile ad albero compatto**
 Lo stile di layout ad albero compatto cerca di costruire una struttura ad albero. Utilizza lo stesso file di input del file[esempio sopra](/diagram/it/java/create-2c-layout-and-auto-fit-shapes/) salva in diversi stili di alberi compatti diversi.

|<p>**Layout ad albero compatto - in basso ea destra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Layout ad albero compatto - in basso ea sinistra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Layout ad albero compatto - a destra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Layout ad albero compatto - a sinistra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Per disporre le forme nello stile ad albero compatto:

1.  Crea un'istanza di[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà dello stile dell'albero compatto.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il file Visio.
#### **Esempio di programmazione in stile albero compatto**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.java" >}}
## **Adatta automaticamente il Visio Diagram**
Aspose.Diagram API supporta l'autoadattamento del disegno Visio. Questa operazione di funzionalità aiuta a portare le forme esterne all'interno del limite di pagina Visio.

Aspose.Diagram for Java API ha la classe Diagram che rappresenta un disegno Visio. La classe DiagramSaveOptions espone la proprietà AutoFitPageToDrawingContent per adattare automaticamente il disegno Visio.

Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Crea un oggetto della classe DiagramSaveOptions e passa il formato di file risultante.
1. Impostare la proprietà AutoFitPageToDrawingContent dell'oggetto DiagramSaveOptions.
1. Chiama il metodo Save dell'oggetto classe Diagram e passa anche il percorso file completo e l'oggetto DiagramSaveOptions.
### **Esempio di programmazione dell'adattamento automatico**
Il codice di esempio seguente mostra come adattare automaticamente le forme nel Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.java" >}}
## **Lavorare con il progetto VBA**
### **Modifica il codice del modulo VBA in Visio Diagram**
Questo articolo mostra come modificare automaticamente il codice di un modulo VBA utilizzando Aspose.Diagram for Java.

Abbiamo aggiunto le classi VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference e VbaProjectReferenceCollection. Queste classi aiutano a ottenere il controllo sul progetto VBA. Gli sviluppatori possono estrarre e modificare il codice del modulo VBA.
### **Modifica l'esempio di programmazione del codice del modulo VBA**
Si prega di controllare questo esempio di codice:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-ModifyVBAModuleCode-ModifyVBAModuleCode.java" >}}
### **Rimuovi tutte le macro da Visio Diagram**
Aspose.Diagram for Java consente agli sviluppatori di rimuovere tutte le macro da Visio diagram.

La proprietà JavaProjectData, esposta da[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, permette di rimuovere tutte le macro dal disegno Visio.
### **Esempio di programmazione Rimuovi tutte le macro**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.java" >}}
