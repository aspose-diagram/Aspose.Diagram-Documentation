---
title: Calcola i valori dei pin e imposta le dimensioni di una forma
type: docs
weight: 40
url: /it/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **Calcola i valori PinX e PinY della forma secondaria**
 Se la forma è un figlio della forma di gruppo, la sua xform è una coordinata relativa della sua forma genitore, ma non una coordinata assoluta nel[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). Se l'utente richiede di ottenere la coordinata assoluta, allora questo codice di esempio aiuta.

Un punto specificato nelle coordinate locali può essere convertito in coordinate padre applicando le seguenti trasformazioni nel seguente ordine:

1. Sottrai il valore della proprietà LocPinX dell'elemento Cell_Type dalla coordinata x.
1. Sottrai il valore della proprietà LocPinY di Cell_Type dalla coordinata y.
1. Eseguire il mirroring del punto sull'asse y se il valore della proprietà FlipX di Cell_Type è uguale a uno.
1. Eseguire il mirroring del punto sull'asse x se il valore della proprietà FlipY di Cell_Type è uguale a uno.
1. Ruotare il punto in senso antiorario attorno all'origine in base al valore della proprietà Angle di Cell_Type.
1. Aggiungi il valore di PinX Cell_Type alla coordinata x.
1. Aggiungi il valore di PinY Cell_Type alla coordinata y.
### **Calcola il campione di programmazione PinX e PinY**
Utilizzare il seguente codice nell'applicazione Java per calcolare i valori PinX e PinY di una forma secondaria utilizzando Aspose.Diagram for Java API.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.java" >}}
## **Impostazione dell'altezza e della larghezza di una forma**
 Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe consente di controllare le dimensioni della forma specificando l'altezza e la larghezza della forma utilizzando i metodi SetHeight e SetWidth.

 I metodi SetHeight e SetWidth, esposti da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)class, supporta il ridimensionamento di una forma con il master, senza il master o sotto forma di una forma di gruppo.

Gli esempi di codice in questo articolo impostano l'altezza e la larghezza per ridimensionare la forma nella pagina.

**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/cTiNWa7.png)

**Il diagram dopo l'altezza e la larghezza sono stati modificati**

![cose da fare:immagine_alt_testo](calculate-pin-values-and-setting-size-of-a-shape_1.png)

Il processo per impostare l'altezza e la larghezza è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Imposta l'altezza di una forma.
1. Imposta la larghezza di una forma.
1. Salva lo diagram.
### **Impostazione dell'altezza e della larghezza Esempio di programmazione**
Il frammento di codice seguente mostra come impostare l'altezza e la larghezza della forma. Il codice cerca un rettangolo con il nome della forma, con l'ID forma 1, e ne imposta l'altezza e la larghezza su double.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ChangeShapeSize-ChangeShapeSize.java" >}}
