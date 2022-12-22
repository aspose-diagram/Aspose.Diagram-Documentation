---
title: Imposta i dati XForm, Line e Fill di Visio Shape
type: docs
weight: 70
url: /it/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Impostazione dei dati XForm**
 L'elemento XForm fa parte dello schema XML Microsoft Visio. XForm specifica la posizione di una forma, ad esempio larghezza, altezza, rotazione e se la forma è stata capovolta. Il[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) proprietà, esposto dal[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, supporta l'oggetto Aspose.Diagram.XForm. La proprietà XForm può essere utilizzata per recuperare o aggiornare i dati XForm di una forma. Gli esempi di codice in questo articolo modificano i valori XForm PinX (coordinata X) e PinY (coordinata Y) per spostare le forme sulla pagina.

**Inserisci diagram** 

![cose da fare:immagine_alt_testo](set-visio-shape-s-xform-line-and-fill-data_1.png)

**Lo diagram dopo il** **PinX** **e** **Pin Y** **i valori sono stati modificati** 

![cose da fare:immagine_alt_testo](set-visio-shape-s-xform-line-and-fill-data_2.png)

Il processo per l'aggiornamento dei dati XForm è:

1. Carica un diagram.# Trova una forma particolare.# Aggiorna i dati XForm della forma.
1. Salva lo diagram.
### **Esempio di programmazione**
Il frammento di codice seguente mostra come aggiornare i dati XForm di una forma. Il codice cerca un processo per i nomi delle forme, con l'ID forma 1, e ne imposta le coordinate X e Y su 5.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetXFormdata-SetXFormdata.java" >}}
## **Impostare Visio dati linea di forma**
Le forme possono essere formattate in diversi modi. Questo articolo mostra come specificare gli attributi di una linea.

Microsoft Visio consente agli utenti di formattare le righe in vari modi. Aspose.Diagram for Java supporta:

- Peso: lo spessore di una linea.
- Colore: imposta il colore della linea della forma.
- Line Color Transparency: imposta la trasparenza del colore della linea della forma in percentuale.
- Motivo: definisce se la linea è continua, tratteggiata o ha un altro motivo.
- Arrotondamento: il raggio degli angoli.
- Frecce di inizio e fine: specificato se la linea ha frecce.
- Dimensioni freccia iniziale e finale: imposta le dimensioni della freccia.
- Cap: termina l'arrotondamento della linea.
### **Modifica il colore della linea, lo spessore, il tipo di trattino, la trasparenza, l'arrotondamento, il tipo di freccia e la dimensione della freccia del bordo di una forma**
 Il[Linea](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) proprietà, esposto dal[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)class, supporta l'oggetto Aspose.Diagram.Line. Questa proprietà può essere utilizzata per recuperare o aggiornare i dati della linea di una forma.
#### **Esempio di programmazione dei dati di linea**
La parte di codice seguente aggiorna i dati della linea di shape.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetLineData-SetLineData.java" >}}
## **Impostare Visio dati di riempimento della forma**
Le forme possono essere formattate in diversi modi. Questo argomento descrive come specificare il riempimento di una forma.

 Microsoft Office Visio consente agli utenti di formattare i riempimenti in vari modi. Il[Riempire](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) classe del Aspose.Diagram for Java API supporta l'impostazione:

- Colori di sfondo e di primo piano.
- Trasparenza.
- Modelli di riempimento.
- Ombre.
### **Impostazione dei valori di riempimento**
La proprietà Fill, esposta dalla classe Shape, supporta l'oggetto Aspose.Diagram.Fill. La proprietà Fill può essere utilizzata per recuperare o aggiornare i dati di riempimento di una forma.

|<p>**L'ingresso diagram** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/OrhEecb.png)</p>|<p>**Il diagram dopo aver cambiato il colore di riempimento** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Esempio di programmazione dei dati di riempimento**
Il frammento di codice seguente aggiorna i dati di riempimento di una forma. Il codice cerca una forma denominata rettangolo, con ID forma 1, e imposta i colori di sfondo e primo piano del riempimento.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetFillData-SetFillData.java" >}}
### **Recupera i dati di riempimento ereditati di una forma Visio**
Le forme Visio possono ereditare lo stile padre e la forma principale. Gli sviluppatori possono ottenere o impostare i dati di riempimento ereditati di una forma Visio. La proprietà InheritFill, esposta dalla classe Shape, contiene i valori di formattazione del riempimento per la forma ereditata dallo stile padre e dalla forma principale.
#### **Esempio di programmazione dei dati di riempimento ereditati Recupera**
Il seguente frammento di codice recupera i dati di riempimento ereditati della forma. Si prega di controllare questo codice di esempio:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveInheritedFillData-RetrieveInheritedFillData.java" >}}
