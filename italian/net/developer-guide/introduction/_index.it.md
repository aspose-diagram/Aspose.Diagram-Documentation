﻿---
title: introduzione
type: docs
weight: 10
url: /it/net/introduction/
description: Introduzione della libreria Aspose.Diagram.
---
## **Ottieni le informazioni sul documento Visio della Biblioteca Aspose.Diagram for .NET**
Microsoft Visio salva le informazioni sulle azioni intraprese su un diagram all'interno del file. Ad esempio, l'ora e la data di creazione del documento, l'ultima volta che è stato modificato, stampato o salvato, vengono salvate con il file. Vengono salvate anche le informazioni su quale versione di Microsoft Visio ha creato e l'ultima modifica del file.

Questo articolo spiega come recuperare tali informazioni.
### **Determinazione della versione di Microsoft Visio che ha creato, modificato e salvato un documento**
 La proprietà Version esposta da[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) la proprietà BuildNumberCreated esposta dalla classe DocumentProperties viene utilizzata per determinare la versione e il numero di build completo dell'istanza Microsoft Visio utilizzata per creare il documento.

 La proprietà BuildNumberEdited esposta da[Proprietà documento](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) class viene utilizzata per determinare il numero di build completo dell'istanza Microsoft Visio utilizzata per modificare il documento.

Le proprietà TimeCreated, TimeEdited, TimePrinted e TimeSaved esposte dalla classe DocumentProperties vengono utilizzate per determinare l'ora in cui il documento Microsoft Visio è stato creato, modificato, stampato e salvato l'ultima volta.

È inoltre possibile impostare queste proprietà per modificare le informazioni nel file. Gli esempi di codice seguenti mostrano come recuperare informazioni su cosa ha creato il file e quando è stato creato, modificato, stampato e salvato.
#### **Esempio di programmazione**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Scrivere Visio Informazioni di riepilogo del documento**
Microsoft Visio consente di definire una serie di proprietà delle informazioni di riepilogo del documento per aiutare te e i tuoi colleghi a identificare un diagram. Le proprietà di riepilogo, ad esempio titolo, oggetto, autore e descrizione, rendono il file più facile da trovare durante la ricerca e più facile da riconoscere quando sfogliare i file.
### **Scrittura Microsoft Visio Documento Sintesi Info**
La classe DocumentProperties espone una serie di proprietà per impostare o ottenere informazioni di riepilogo Microsoft Visio diagram. Aspose.Diagram for .NET può aggiornare le informazioni di riepilogo del disegno e quindi riscrivere il file di disegno in VDX.

{{% alert color="primary" %}} 

Si prega di notare che non è possibile impostare valori rispetto a**Applicazione**e**Produttore**campi, perché Aspose Ltd. e Aspose.Diagram for .NET xxx verranno visualizzati su questi campi.

{{% /alert %}} 

Per aggiornare le informazioni di riepilogo del disegno di un file VDX o VSD esistente:

1.  Crea un'istanza di[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) classe.
1.  Imposta le proprietà esposte da[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) per definire le informazioni di riepilogo per il file di disegno Visio.
1. Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VDX.

Controlla le informazioni di riepilogo:

1. Aprire il file di output VDX in Microsoft Visio.
1. Selezionando Info dal menu File.
#### **Scrittura Visio Informazioni di riepilogo del documento Esempio di programmazione**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Rileva il formato del file Visio**
Utilizzando Aspose.Diagram for .NET API, gli sviluppatori possono rilevare il formato del file Visio prima di aprirlo perché l'estensione del file non garantisce che il contenuto del file sia appropriato.
### **Rileva campione di programmazione del formato**
Il seguente codice di esempio illustra come rilevare un formato di file (utilizzando il percorso o il flusso del file) e controllarne l'estensione.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
