﻿---
title: Ruota, cambia la posizione e collega le forme secondarie
type: docs
weight: 60
url: /it/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Ruota una forma con l'angolo adatto**
 Aspose.Diagram for Java consente di ruotare una forma a qualsiasi angolazione. Il metodo SetAngle esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class può essere utilizzato per ruotare una forma a qualsiasi angolo desiderato. Prende un singolo parametro come angolo.
### **Ruotare un esempio di programmazione delle forme**
Utilizzare il seguente codice nell'applicazione Java per ruotare una forma utilizzando Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RotateVisioShape-RotateVisioShape.java" >}}
## **Modificare la posizione di una forma**
La classe Shape consente di modificare la posizione di una forma. La linea del connettore si regola automaticamente quando la forma viene spostata in una posizione diversa.

I metodi Move e MoveTo, esposti dalla classe Shape, supportano o meno la modifica della posizione di una forma come parte di un gruppo.
Gli esempi di codice in questo articolo spostano una forma nella pagina.
**Inserisci diagram** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/cThgWnB.png)


**Il diagram dopo che la forma è stata spostata** 

![cose da fare:immagine_alt_testo](http://i.imgur.com/Q3QByqe.png)

Il processo per spostare una forma è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Sposta la forma in una posizione diversa
1. Salva lo diagram.
### **Esempio di programmazione della modifica della posizione**
Il frammento di codice seguente mostra come spostare la forma. Il codice recupera una pagina Visio per nome e forma per ID 16 e ne sposta la posizione.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-MoveVisioShape-MoveVisioShape.java" >}}
## **Collega le forme secondarie dei gruppi**
Questo argomento elabora come collegare due forme secondarie di due diverse forme di gruppo nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for Java.

 Il metodo ConnectShapesViaConnector esposto da[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class può essere utilizzata per connettere le forme tramite i loro ID. Il metodo AddShape, esposto da[Diagram](https://reference.aspose.com/diagram/java)class, può essere utilizzato per aggiungere una forma.

|<p>**L'ingresso diagram** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/74rDby5.png)</p>|<p>**Il diagram dopo il collegamento di sotto-forme** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una determinata pagina.
1. Aggiungi la forma del connettore dinamico alla pagina selezionata.
1. Connetti sotto-forme
### **Esempio di programmazione Connect Sub-shapes**
Utilizzare il seguente codice nell'applicazione Java per collegare le forme secondarie di due diverse forme di gruppo utilizzando Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.java" >}}
## **Ottieni le forme collegate a una forma particolare**
[Aggiungi e collega Visio Forme](/diagram/it/java/add-and-connect-visio-shapes/) spiega come aggiungere una forma e collegarla ad altre forme nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for Java. È anche possibile trovare forme collegate a una forma specifica.

 Il metodo ConnectedShapes esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class può essere utilizzata per ottenere gli ID delle forme connesse a una forma. Il metodo GetShape, esposto da[Collezione Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, può quindi essere utilizzato per trovare una forma in base al relativo ID.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Ottieni i nomi di tutte le forme collegate alla forma selezionata.
### **Ottieni un esempio di programmazione di forme**
Usa il seguente codice nella tua applicazione Java per trovare tutte le forme collegate a una forma specifica usando Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.java" >}}
