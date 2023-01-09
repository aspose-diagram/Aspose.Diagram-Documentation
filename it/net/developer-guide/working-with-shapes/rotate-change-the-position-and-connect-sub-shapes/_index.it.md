---
title: Ruota, cambia la posizione e collega le forme secondarie
type: docs
weight: 30
url: /it/net/rotate-change-the-position-and-connect-sub-shapes/
description: Questa sezione spiega come ruotare una forma visio con Aspose.Diagram.
---
## **Ruota una forma con l'angolo adatto**
 Aspose.Diagram for .NET consente di ruotare una forma a qualsiasi angolazione. Il metodo SetAngle esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class può essere utilizzato per ruotare una forma a qualsiasi angolo desiderato. Prende un singolo parametro come angolo.
### **Ruotare un esempio di programmazione delle forme**
Utilizzare il seguente codice nell'applicazione .NET per ruotare una forma utilizzando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RotateVisioShape-RotateVisioShape.cs" >}}
## **Modificare la posizione di una forma**
 Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe consente di modificare la posizione di una forma. La linea del connettore si regola automaticamente quando la forma viene spostata in una posizione diversa. I metodi Move e MoveTo, esposti da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, supporto per cambiare la posizione di una forma come parte di un gruppo o meno. Gli esempi di codice in questo articolo spostano una forma nella pagina.

Il processo per spostare una forma è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Sposta la forma in una posizione diversa
1. Salva lo diagram.
### **Esempio di programmazione della modifica della posizione**
Il frammento di codice seguente mostra come spostare la forma. Il codice recupera una pagina Visio per nome e forma per ID 16 e ne sposta la posizione.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-MoveVisioShape-MoveVisioShape.cs" >}}
## **Collega le forme secondarie dei gruppi**
 Questo argomento elabora come connettere due forme secondarie di due diverse forme di gruppo nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for .NET. Il metodo ConnectShapesViaConnector esposto dal[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class può essere utilizzata per connettere le forme tramite i loro ID. Il metodo AddShape, esposto da[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class, può essere utilizzato per aggiungere una forma.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una determinata pagina.
1. Aggiungi la forma del connettore dinamico alla pagina selezionata.
1. Connetti sotto-forme
### **Esempio di programmazione Connect Sub-shapes**
Utilizzare il seguente codice nell'applicazione .NET per collegare le forme secondarie di due diverse forme di gruppo utilizzando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.cs" >}}
## **Ottieni le forme collegate a una forma particolare**
[Aggiungi e collega Visio Forme](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) spiega come aggiungere una forma e collegarla ad altre forme nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for .NET. È anche possibile trovare forme collegate a una forma specifica.

 Il metodo ConnectedShapes esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class può essere utilizzata per ottenere gli ID delle forme connesse a una forma. Il metodo GetShape, esposto da[Collezione Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, può quindi essere utilizzato per trovare una forma in base al relativo ID.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Ottieni i nomi di tutte le forme collegate alla forma selezionata.
### **Ottieni un esempio di programmazione di forme**
Usa il seguente codice nella tua applicazione .NET per trovare tutte le forme collegate a una forma specifica usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.cs" >}}
