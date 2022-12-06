---
title: Lavorare con l'incollaggio di forme
type: docs
weight: 40
url: /it/net/working-with-shapes-gluing/
description: Questa sezione spiega come ottenere forme incollate a una particolare forma con Aspose.Diagram.
---
## **Ottieni i connettori incollati a una forma particolare**
[Aggiungi e collega Visio Forme](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) spiega come aggiungere una forma e collegarla ad altre forme nei diagrammi Microsoft Visio utilizzando Aspose.Diagram for .NET. È anche possibile trovare connettori incollati a questa forma.
### **Ottenere forme incollate**
 Il metodo GluedShapes esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class può essere utilizzata per ottenere un elenco degli ID di tutti i connettori associati a una forma oppure, se la forma in questione è un connettore, gli ID delle forme a cui è connessa. Il metodo GetShape, esposto dalla[Collezione Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, può quindi essere utilizzato per trovare una forma in base al relativo ID.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Ottieni un elenco di ID di tutti i connettori incollati a questa forma.
#### **Ottieni un esempio di programmazione di connettori incollati**
Usa il seguente codice nella tua applicazione .NET per trovare tutti i connettori incollati a una forma usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GetGluedConnectors-GetGluedConnectors.cs" >}}
## **Colla Visio Forme insieme al punto di connessione**
Aspose.Diagram for .NET consente agli sviluppatori di incollare forme insieme attraverso i punti di connessione.
### **Forme di colla**
 Il metodo GlueShapes esposto da[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe può essere utilizzata.

|<p>**Inserisci diagram** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_1.png)</p>|<p>**Lo diagram dopo aver incollato le sagome** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Forme di colla.
1. Salva diagram.
#### **Colla Visio Esempio di programmazione delle forme**
Usa il seguente codice nella tua applicazione .NET per incollare le forme attraverso i punti di connessione:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueVisioShapes-GlueVisioShapes.cs" >}}
## **Forme di colla all'interno del contenitore**
Aspose.Diagram for .NET consente agli sviluppatori di incollare forme di gruppo all'interno di un contenitore.
### **Forma del gruppo di colla**
 Il metodo GlueShapesInContainer esposto da[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe può essere utilizzata.

|<p>**Inserisci diagram** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_3.png)</p>|<p>**Lo diagram dopo aver incollato le sagome di gruppo** </p><p>![cose da fare:immagine_alt_testo](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. Incolla le forme del gruppo.
1. Salva diagram.
#### **Forme di colla all'interno dell'esempio di programmazione**
Usa il seguente codice nella tua applicazione .NET per incollare la forma del gruppo all'interno di un contenitore:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueContainerShape-GlueContainerShape.cs" >}}
