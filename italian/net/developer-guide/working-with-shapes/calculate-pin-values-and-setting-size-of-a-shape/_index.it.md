---
title: Calcola i valori dei pin e imposta le dimensioni di una forma
type: docs
weight: 60
url: /it/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Questa sezione spiega come calcolare i valori PinX e PinY della Sub Shape con Aspose.Diagram.
---
## **Calcola i valori PinX e PinY della forma secondaria**
 Se la forma è un nodo figlio di una forma di gruppo, la sua forma x è una coordinata relativa della sua forma padre ma non una coordinata assoluta nel[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Se l'utente richiede di ottenere la coordinata assoluta, allora questo codice di esempio aiuta.

Un punto specificato nelle coordinate locali può essere convertito in coordinate padre applicando le seguenti trasformazioni nel seguente ordine:

1. Sottrai il valore della proprietà LocPinX dell'elemento Cell_Type dalla coordinata x.
1. Sottrai il valore della proprietà LocPinY di Cell_Type dalla coordinata y.
1. Eseguire il mirroring del punto sull'asse y se il valore della proprietà FlipX di Cell_Type è uguale a uno.
1. Eseguire il mirroring del punto sull'asse x se il valore della proprietà FlipY di Cell_Type è uguale a uno.
1. Ruotare il punto in senso antiorario attorno all'origine in base al valore della proprietà Angle di Cell_Type.
1. Aggiungi il valore di PinX Cell_Type alla coordinata x.
1. Aggiungi il valore di PinY Cell_Type alla coordinata y.
### **Calcola il campione di programmazione PinX e PinY**
Utilizzare il seguente codice nell'applicazione .NET per calcolare i valori PinX e PinY di una forma secondaria utilizzando Aspose.Diagram for .NET API.







{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.cs" >}}
## **Impostazione dell'altezza e della larghezza di una forma**
 Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe consente di controllare le dimensioni della forma specificando l'altezza e la larghezza della forma utilizzando i metodi SetHeight e SetWidth.

 I metodi SetHeight e SetWidth, esposti da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, supporta il ridimensionamento di una forma con il master, senza il master o sotto forma di una forma di gruppo. Gli esempi di codice in questo articolo impostano l'altezza e la larghezza per ridimensionare la forma nella pagina.

Il processo per impostare l'altezza e la larghezza è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Imposta l'altezza di una forma.
1. Imposta la larghezza di una forma.
1. Salva lo diagram.
### **Impostazione dell'altezza e della larghezza Esempio di programmazione**
Il frammento di codice seguente mostra come impostare l'altezza e la larghezza della forma. Il codice cerca un rettangolo con il nome della forma, con l'ID forma 1, e ne imposta l'altezza e la larghezza su double.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ChangeShapeSize-ChangeShapeSize.cs" >}}
