---
title: Imposta i dati XForm, Line e Fill di Visio Shape
type: docs
weight: 20
url: /it/net/set-visio-shape-s-xform-line-and-fill-data/
description: Questa sezione spiega come impostare lo stile della forma, inclusi i dati della linea e i dati di riempimento con Aspose.Diagram.
---
## **Impostazione dei dati XForm**
 L'elemento XForm fa parte dello schema XML Microsoft Visio. XForm specifica la posizione di una forma, ad esempio larghezza, altezza, rotazione e se la forma è stata capovolta. Il[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) proprietà, esposto dal[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, supporta l'oggetto Aspose.Diagram.XForm. La proprietà XForm può essere utilizzata per recuperare o aggiornare i dati XForm di una forma. Gli esempi di codice in questo articolo modificano i valori XForm PinX (coordinata X) e PinY (coordinata Y) per spostare le forme sulla pagina.

Il processo per l'aggiornamento dei dati XForm è:

1. Carica un diagram.# Trova una forma particolare.# Aggiorna i dati XForm della forma.
1. Salva lo diagram.
### **Esempio di programmazione**
Il frammento di codice seguente mostra come aggiornare i dati XForm di una forma. Il codice cerca un processo per i nomi delle forme, con l'ID forma 1, e ne imposta le coordinate X e Y su 5.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **Impostare Visio dati linea di forma**
Le forme possono essere formattate in diversi modi. Questo articolo mostra come specificare gli attributi di una linea.

Microsoft Visio consente agli utenti di formattare le righe in vari modi. Aspose.Diagram for .NET supporta:

- Peso: lo spessore di una linea.
- Colore: imposta il colore della linea della forma.
- Line Color Transparency: imposta la trasparenza del colore della linea della forma in percentuale.
- Motivo: definisce se la linea è continua, tratteggiata o ha un altro motivo.
- Arrotondamento: il raggio degli angoli.
- Frecce di inizio e fine: specificato se la linea ha frecce.
- Dimensioni freccia iniziale e finale: imposta le dimensioni della freccia.
- Cap: termina l'arrotondamento della linea.
### **Modifica il colore della linea, lo spessore, il tipo di trattino, la trasparenza, l'arrotondamento, il tipo di freccia e la dimensione della freccia del bordo di una forma**
 Il[Linea](http://www.aspose.com/api/net/diagram/aspose.diagram/line) proprietà, esposto dal[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, supporta l'oggetto Aspose.Diagram.Line. Questa proprietà può essere utilizzata per recuperare o aggiornare i dati della linea di una forma.
#### **Esempio di programmazione dei dati di linea**
La parte di codice seguente aggiorna i dati della linea di shape.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **Impostare Visio dati di riempimento della forma**
 Le forme possono essere formattate in diversi modi. Questo argomento descrive come specificare il riempimento di una forma. Microsoft Office Visio consente agli utenti di formattare i riempimenti in vari modi. Il[Riempire](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) classe del Aspose.Diagram for .NET API supporta l'impostazione:

- Colori di sfondo e di primo piano.
- Trasparenza.
- Modelli di riempimento.
- Ombre.
### **Impostazione dei valori di riempimento**
 La proprietà Fill, esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, supporta il[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) oggetto. La proprietà Fill può essere utilizzata per recuperare o aggiornare i dati di riempimento di una forma.
#### **Esempio di programmazione dei dati di riempimento**
Il frammento di codice seguente aggiorna i dati di riempimento di una forma. Il codice cerca una forma denominata rettangolo, con ID forma 1, e imposta i colori di sfondo e primo piano del riempimento.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **Recupera i dati di riempimento ereditati di una forma Visio**
 Le forme Visio possono ereditare lo stile padre e la forma master. Gli sviluppatori possono ottenere o impostare i dati di riempimento ereditati di una forma Visio. La proprietà InheritFill, esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene i valori di formattazione del riempimento per la forma ereditata dallo stile principale e dalla forma principale.
#### **Esempio di programmazione dei dati di riempimento ereditati Recupera**
Il seguente frammento di codice recupera i dati di riempimento ereditati della forma. Si prega di controllare questo codice di esempio:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
