---
title: Aspose.Diagram for Java 17.7 Note di rilascio
type: docs
weight: 60
url: /it/java/aspose-diagram-for-java-17-7-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 17.7](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-7-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50491|Impossibile recuperare la nuova altezza della forma formulata.|Aumento|
|DIAGRAMJAVA-50510|VSD in SVG - modello di colore di riempimento errato nelle forme.|Aumento|
|DIAGRAMJAVA-50483|Connessione incompleta delle forme durante il salvataggio di un disegno nel formato VSDX.|Insetto|
|DIAGRAMJAVA-50488|Ulteriori elementi di testo vengono aggiunti durante la conversione di un VSD in SVG.|Insetto|
|DIAGRAMJAVA-50490|Le linee del bordo verticale della casella del processo predefinito sono spesse durante la generazione di un disegno VSDX.|Insetto|
|DIAGRAMJAVA-50495|Output VSDX - layout errato della linea del connettore durante l'aggiunta di testo alle forme.|Insetto|
|DIAGRAMJAVA-50496|Uscita VSDX - tutti i connettori sono spostati verso l'alto.|Insetto|
|DIAGRAMJAVA-50498|Output VSDX - la visualizzazione del testo verticale delle forme invece dell'orizzontale.|Insetto|
|DIAGRAMJAVA-50506|Si è verificato un errore durante il caricamento di un disegno VDX.|Insetto|
|DIAGRAMJAVA-50508|Output VSDX - l'overflow del testo durante l'aggiunta di testo su più righe.|Insetto|
|DIAGRAMJAVA-50511|Output VSDX - testo fuori posizione del connettore dinamico.|Insetto|
|DIAGRAMJAVA-50512|Output VSDX - la linea di collegamento che passa attraverso un'altra forma|Insetto|
|DIAGRAMJAVA-50513|Output VSDX - una linea aggiuntiva di connettore all'interno della forma decisionale|Insetto|
|DIAGRAMJAVA-50515|Output VSDX - l'intero testo della forma è fuori dal bordo|Insetto|
### **Il metodo addComment viene aggiunto nella classe Page**
Un metodo addComment sottoposto a overload, esposto dalla classe Page accetta un'istanza della classe Shape e una stringa di testo del commento.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Aggiungere un commento a livello di forma nel disegno Visio](/diagram/it/java/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
