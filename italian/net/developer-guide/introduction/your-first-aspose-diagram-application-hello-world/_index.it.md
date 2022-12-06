---
title: La tua prima domanda Aspose.Diagram - Hello World
type: docs
weight: 30
url: /it/net/your-first-aspose-diagram-application-hello-world/
description: Questa pagina descrive come creare la prima applicazione con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

Questo tutorial mostra come creare una primissima applicazione (Hello World) usando Aspose.Diagram' semplice API. Questa semplice applicazione crea un file Microsoft Visio con il testo 'Hello World' in una pagina specificata.

{{% /alert %}}

## **Creazione dell'applicazione Hello World**

passaggi seguenti creano l'applicazione Hello World utilizzando Aspose.Diagram API:

1.  Crea un'istanza di[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) classe.
1.  Se hai una licenza, allora[applicarlo](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Se stai utilizzando la versione di valutazione, salta le righe di codice relative alla licenza.
1. Crea un nuovo file Visio o apri un file Visio esistente.
1. Crea una nuova casella di testo.
1.  Inserisci le parole**Ciao mondo!** in una casella di testo.
1. Generare il file Microsoft Visio modificato.

L'implementazione dei passaggi precedenti è dimostrata negli esempi seguenti.

### **Esempio di codice: creazione di un nuovo Diagram**

L'esempio seguente crea un nuovo diagram da zero, scrive Hello World! nella prima pagina e salva il file Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateNewVisio-CreateNewVisio.cs" >}}

### **Esempio di codice: apertura di un file esistente**

L'esempio seguente apre un file modello Microsoft Visio esistente denominato "Sample.vsdx", inserisce "Hello World!" testo nella prima pagina e salva lo diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ReadVisioDiagram-ReadVisioDiagram.cs" >}}
