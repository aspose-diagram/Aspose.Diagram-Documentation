---
title: introduzione
type: docs
weight: 10
url: /it/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio salva le informazioni sulle azioni intraprese su un diagram all'interno del file. Ad esempio, l'ora e la data di creazione del documento, l'ultima volta che è stato modificato, stampato o salvato, vengono salvate con il file. Vengono salvate anche le informazioni su quale versione di Microsoft Visio ha creato e l'ultima modifica del file.

Questo articolo spiega come recuperare tali informazioni.

{{% /alert %}} 
## **Ottieni la versione della libreria Aspose.Diagram for Java**
 Il memthod getVersion() esposto da[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) e il metodo getBuildNumberCreated() esposto da[Proprietà documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) vengono utilizzate per determinare la versione e il numero di build completo dell'istanza Microsoft Visio utilizzata per creare il documento.
### **Determinazione della versione di Microsoft Visio che ha creato, modificato e salvato un documento**
 Il metodo getBuildNumberEdited() esposto da[Proprietà documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class viene utilizzata per determinare il numero di build completo dell'istanza Microsoft Visio utilizzata per modificare il documento.

 metodi getTimeCreated(), getTimeEdited(), getTimePrinted() e getTimeSaved() esposti dal[Proprietà documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) vengono utilizzate per determinare l'ora in cui il documento Microsoft Visio è stato creato, l'ultima modifica, l'ultima stampa e l'ultimo salvataggio.

È inoltre possibile impostare queste proprietà per modificare le informazioni nel file.

Gli esempi di codice seguenti mostrano come recuperare informazioni su cosa ha creato il file e quando è stato creato, modificato, stampato e salvato.

**L'output del codice in una finestra della console** 

![cose da fare:immagine_alt_testo](introduction_1.png)
#### **Esempio di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-GetLibraryVersion-GetLibraryVersion.java" >}}
## **Scrittura Microsoft Visio Documento Sintesi Info**
Microsoft Visio consente di definire una serie di proprietà delle informazioni di riepilogo del documento per aiutare te e i tuoi colleghi a identificare un diagram. Le proprietà di riepilogo, ad esempio titolo, oggetto, autore e descrizione, rendono il file più facile da trovare durante la ricerca e più facile da riconoscere durante la navigazione File.

 Il[Proprietà documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)class espone una serie di proprietà da impostare o ottenere informazioni di riepilogo Microsoft Visio diagram. Aspose.Diagram for Java può aggiornare le informazioni di riepilogo del disegno e quindi riscrivere il file di disegno in VDX.

{{% alert color="primary" %}} 

Si prega di notare che non è possibile impostare valori rispetto a**Applicazione**e**Produttore**campi, perché Aspose Ltd. e Aspose.Diagram for Java xxx verranno visualizzati su questi campi.

{{% /alert %}} 
### **Scrittura Microsoft Visio Documento Sintesi Info**
Per aggiornare le informazioni di riepilogo del disegno di un file VDX o VSD esistente:

1.  Crea un'istanza di[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) classe.
1. Impostare le proprietà esposte dal metodo Diagram.getDocumentProps() per definire le informazioni di riepilogo per il file di disegno Visio.
1. Chiamare il metodo save() della classe Diagram per scrivere il file di disegno Visio in VDX.

Controlla le informazioni di riepilogo:

1. Aprire il file di output VDX in Microsoft Visio.
1.  Selezione**Informazioni** dal**File** menù.

**La finestra di dialogo Informazioni che mostra le informazioni di riepilogo aggiornate** 

![cose da fare:immagine_alt_testo](introduction_2.png)
#### **Esempio di programmazione**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-SetVisioProperties-SetVisioProperties.java" >}}
## **Rileva il formato di un file Visio**
 Usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, gli sviluppatori possono rilevare il formato del file Visio prima di aprirlo perché l'estensione del file non garantisce che il contenuto del file sia appropriato.
### **Rileva campione di programmazione del formato**
Il seguente codice di esempio illustra come rilevare un formato di file (utilizzando il percorso o il flusso del file) e controllarne l'estensione.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.java" >}}
## **Rileva il formato di un file Visio da un InputStream**
Utilizzando Aspose.Diagram for Java API, gli sviluppatori possono rilevare il formato di un file Visio passando un flusso di input. Il metodo detectFileFormat della classe FileFormatUtil può essere utilizzato per raggiungere questo obiettivo.
### **Rileva il formato da un esempio di programmazione InputStream**
Il codice di esempio seguente illustra come rilevare un formato di file utilizzando un flusso di input.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}
