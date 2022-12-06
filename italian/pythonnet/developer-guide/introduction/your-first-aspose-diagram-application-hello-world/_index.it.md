---
title: La tua prima domanda Aspose.Diagram - Hello World
type: docs
weight: 30
url: /it/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

Questo argomento per principianti mostra come gli sviluppatori possono creare una semplice prima applicazione (Hello World) utilizzando Aspose.Diagram' simple API. L'applicazione crea un file Microsoft Visio con le parole Hello World nella pagina.

{{% /alert %}}

### **Creazione dell'applicazione Hello World**

Per creare l'applicazione Hello World utilizzando Aspose.Diagram API:

1. Creare un'istanza della classe Workbook.
1. Applica la licenza:
 1. Se hai acquistato una licenza, usa la licenza nella tua applicazione per ottenere l'accesso alla piena funzionalità di Aspose.Diagram
 1. Se stai utilizzando la versione di valutazione del componente (se stai utilizzando Aspose.Diagram senza licenza), salta questo passaggio.
1. Crea un nuovo file Microsoft Visio o apri un file esistente in cui desideri aggiungere/aggiornare del testo.
1.  Inserisci le parole**Ciao mondo!** nella pagina a cui si accede.
1. Generare il file Microsoft Visio modificato.

Gli esempi seguenti illustrano i passaggi precedenti.

#### **Creazione di un numero Diagram**

L'esempio seguente crea un nuovo diagram da zero, scrive le parole "Hello World!" sulla prima pagina e salva il file.

**Crea un nuovo file visio** 

![cose da fare:immagine_alt_testo](your-first-aspose-diagram-application-hello-world_1.png)

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **Apertura di un file esistente**

L'esempio seguente apre un file modello Microsoft Visio esistente, scrive le parole "Hello World!" nella prima pagina e salva lo diagram come nuovo file.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
