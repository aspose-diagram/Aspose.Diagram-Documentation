---
title: Lavorare con i Maestri
type: docs
weight: 70
url: /it/net/working-with-masters/
description: Questa sezione spiega come aggiungere master o ottenere informazioni master con Aspose.Diagram.
---
## **Recupero delle informazioni sul master**
Uno shape master è un altro nome per uno stencil Visio. Con Aspose.Diagram è possibile recuperare informazioni su pagine, connettori e anche master. Questo articolo spiega come ottenere l'ID e il nome da uno diagram.

 Il[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'oggetto rappresenta a[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) master dell'oggetto in un oggetto diagram. La proprietà Masters, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Master. Questa proprietà può essere utilizzata per recuperare le informazioni sui master, ovvero l'ID e il nome del master. Utilizzare la proprietà Page.Shapes per determinare quale forma è stata ereditata dalla forma master.
### **Recupero del campione di programmazione delle informazioni principali**
Il seguente pezzo di codice recupera le informazioni master da un diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-RetrieveMasterInfo-RetrieveMasterInfo.cs" >}}
## **Aggiungi Master dallo Stencil di forme**
Uno stencil è una raccolta di forme associate a un particolare modello Microsoft Office Visio. Con Aspose.Diagram è possibile aggiungere qualsiasi modello di forma a un disegno da uno stencil.
### **Aggiungi Maestro**
 Il[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) l'oggetto rappresenta a[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) master dell'oggetto in un diagram. Il metodo AddMaster, esposto dalla classe Diagram, consente di aggiungere un master da uno stencil. Offre le seguenti quattro modalità:

- Percorso file stencil e ID master.
- Percorso file stencil e nome master.
- Flusso di file di stencil e ID principale.
- Flusso di file di stencil e nome principale.
- Aggiungi master a diagram dalla fonte diagram
#### **Aggiungi un esempio di programmazione principale**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-AddMasterFromStencil-AddMasterFromStencil.cs" >}}
## **Crea Master da zero**
 Aspose.Diagram API permette di creare un[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) da zero senza alcuno stencil, disegno o modello. Gli sviluppatori possono personalizzare la creazione di Master. Il metodo AddMaster, esposto dalla classe Diagram, permette di aggiungere un master.
### **Crea un esempio di programmazione principale**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateMasterFromScratch-CreateMasterFromScratch.cs" >}}
## **Ottieni un master dal file Visio**
A volte, gli sviluppatori devono ottenere i dettagli del master di un disegno Visio. Il Aspose.Diagram API supporta questa funzione.

 Aspose.Diagram for .NET offre il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class che rappresenta un disegno Visio. La proprietà Masters, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Master. Questa proprietà può essere utilizzata per recuperare i dettagli di un particolare master. La classe MasterCollection espone i metodi GetMasterByName e GetMaster che possono essere chiamati per ottenere un oggetto Master.
### **Ottenere un oggetto master per ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiama il metodo GetMaster della classe Diagram.Masters.
#### **Oggetto principale per esempio di programmazione ID**
L'esempio seguente mostra come ottenere un master per ID da un disegno Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyID-GetMasterbyID.cs" >}}
### **Ottenere un oggetto principale per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo GetMasterByName della classe Diagram.Masters.
#### **Esempio di programmazione oggetto master per nome**
L'esempio seguente mostra come ottenere un oggetto principale per nome da un disegno Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyName-GetMasterbyName.cs" >}}
## **Verificare Presenza di un Maestro nel Disegno Visio**
Il Aspose.Diagram API supporta il controllo della presenza di un master in un disegno Visio. Con la proprietà MasterCollection, gli sviluppatori possono verificare se un master è presente in base al nome o all'ID.

 Aspose.Diagram for .NET offre il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio. La proprietà Masters, esposta dalla classe Diagram, supporta una raccolta di oggetti Aspose.Diagram.Master. Questa proprietà può essere utilizzata per verificare la presenza di un particolare master. La classe MasterCollection espone il metodo IsExist che può essere chiamato con il nome master o il parametro ID.
### **Controllo di una presenza principale tramite ID**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo IsExist della classe Diagram.Masters.
#### **Presenza principale tramite esempio di programmazione ID**
L'esempio seguente mostra come verificare la presenza di un master per ID in un disegno Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.cs" >}}
### **Controllo di una presenza principale per nome**
Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Chiamare il metodo IsExist della classe Diagram.Masters.
#### **Esempio di programmazione della presenza principale per nome**
L'esempio seguente mostra come controllare una presenza master per nome dal disegno Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.cs" >}}
