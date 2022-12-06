---
title: Lavorare con il testo
type: docs
weight: 120
url: /it/java/working-with-text/
---
## **Inserisci una forma di testo nella pagina Visio**
 Aspose.Diagram API consente agli sviluppatori di inserire una forma di testo ovunque nella pagina Visio. Per raggiungere questo obiettivo, il metodo addText di[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class accetta i parametri PinX, PinY, larghezza, altezza e testo.
### **Inserisci un esempio di programmazione di forme di testo**
Il seguente pezzo di codice aggiunge una forma di testo nel Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-InsertTextShape-InsertTextShape.java" >}}
## **Aggiorna Visio Forma testo**
 Così come[creazione di diagrammi](/diagram/it/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java consente di lavorare con le forme in modi diversi. Questo articolo illustra come accedere e aggiornare il testo nelle forme.

 La proprietà Text, esposta da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, supporta l'oggetto Aspose.Diagram.Text. La proprietà può essere utilizzata per recuperare o aggiornare il testo di una forma.

**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/6aEp7h0.png)

**Diagram dopo che il testo nella forma centrale è stato modificato da Processo a Nuovo testo** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/o977cxw.png)

Il processo per aggiornare il testo di una forma è semplice:

1. Carica un diagram.
1. Trova una forma particolare.
1. Imposta il nuovo testo.
1. Salva lo diagram.
### **Aggiornamento dell'esempio di programmazione del testo della forma**
Il seguente pezzo di codice aggiorna il testo di una forma. Le forme sono identificate dai relativi ID. I segmenti di codice seguenti cercano una forma chiamata processo e con l'ID 1 e ne modificano il testo.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-UpdateShapeText-UpdateShapeText.java" >}}
## **Applicare il foglio di stile integrato o personalizzato a una forma Visio**
fogli di stile Microsoft Visio memorizzano le informazioni di formattazione che possono essere applicate alle forme per un aspetto coerente. Aspose.Diagram for Java consente di applicare fogli di stile dall'interno di un'applicazione.

 Le proprietà TextStyle, FillStyle e LineStyle esposte da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) classe sostenere il[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) oggetto. La proprietà può essere utilizzata per recuperare informazioni sullo stile e applicare stili di testo, linea e riempimento personalizzati a un diagram.

**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/feV1x2N.png)

**Il diagram dopo aver applicato un foglio di stile personalizzato che definisce gli stili di testo, linea e riempimento** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/Xk9W0wN.png)
### **Stili personalizzati in Microsoft Visio**
Per applicare stili personalizzati alle forme in Microsoft Visio:

1. Apri uno diagram in Microsoft Visio.
1.  Selezionare**Definisci stili** dal**Formato** menu (Visio 2007) o fare clic con il pulsante destro del mouse**Stili** nel**Esploratore di disegni** finestra e selezionare**Definisci stili** (Visio 2010).
1.  Nel**Definisci stili** finestra di dialogo, digitare un nuovo nome per il foglio di stile personalizzato. Ad esempio, CustomStyle1.
1.  Clicca il**Testo**, **Linea** e**Riempire** pulsanti per impostare rispettivamente gli stili di testo, linea e riempimento.
1.  Clic**OK**.

Dopo aver definito i fogli di stile personalizzati in Microsoft Visio, utilizzare il seguente codice in un'applicazione Java per applicare stili personalizzati alle forme. Si noti che gli esempi di codice seguenti richiamano il foglio di stile personalizzato definito sopra: è necessario conoscere il nome e la posizione del foglio che si applica.

Per applicare gli stili personalizzati a livello di codice:

1. Carica un diagram.
1. Trova la forma a cui vuoi applicare uno stile.
1. Carica il foglio di stile.
1. Applicare stili.
1. Salva lo diagram.
#### **Applicare l'esempio di programmazione di stili personalizzati**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.java" >}}
## **Applica uno stile diverso a ciascun valore di testo di una forma**
 Così come[creazione di diagrammi](/diagram/it/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java consente di lavorare con le forme in modi diversi. Questo articolo aiuta ad aggiungere più valori di testo a una forma e ad applicare uno stile diverso a ogni valore di testo.

{{% alert color="primary" %}} 

L'elemento Shape contiene un elemento chiamato Text, che contiene i caratteri del testo e gli elementi speciali (cp, pp, tp e fld) che segnano la fine di un'esecuzione e l'inizio della successiva. L'elemento Char contiene gli attributi di formattazione per il testo della forma, come carattere, colore, stile del testo, maiuscole e minuscole, posizione rispetto alla linea di base e dimensione in punti.

{{% /alert %}} 
### **Aggiunta di forme di testo e stili**
**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/ZqgQPQC.png)

**Diagram dopo aver aggiunto vari valori di testo a una forma con uno stile diverso su ciascun valore di testo** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/7UWhFbU.png)
#### **Esempio di programmazione dell'aggiunta di testo e stili**
Il seguente pezzo di codice aggiunge il testo di una forma e diversi stili.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-ApplyFontOnText-ApplyFontOnText.java" >}}
## **Trova e sostituisci il testo di una forma**
 Il[Testo](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) La classe ti consente di modificare il testo della forma. Il metodo Replace, esposto da[Testo](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) class, supporta la modifica del testo di una forma.
Gli esempi di codice in questo articolo trovano e sostituiscono il testo della forma nella pagina.

**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/lW5xaP0.png)


**Il diagram dopo che la forma è stata modificata** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/m33W1Tk.png)

Il processo per modificare il testo della forma:

1. Carica un diagram.
1. Trova un particolare testo di una forma.
1. Sostituisci il testo di questa forma
1. Salva lo diagram.
### **Esempio di programmazione di testo Trova e sostituisci**
I frammenti di codice seguenti mostrano come modificare il testo della forma. Il codice scorre le forme di una pagina.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.java" >}}
## **Estrai testo normale dalla pagina Visio Diagram**
Aspose.Diagram API consente agli sviluppatori di estrarre testo normale dalla pagina Visio diagram. Possono anche scorrere le pagine Visio diagram per coprire l'intero testo Visio diagram.

 Microsoft Office Visio aggiunge il testo alle forme. Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class contiene un elemento chiamato Text, che contiene i caratteri del testo e gli elementi speciali (cp, pp, tp e fld) che segnano la fine di un'esecuzione e l'inizio della successiva.
### **Estrai un esempio di programmazione in testo normale**
La parte di codice seguente scorre le forme della pagina Visio e filtra il testo normale senza informazioni di formattazione.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.java" >}}
