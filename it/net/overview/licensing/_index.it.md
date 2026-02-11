---
title: Licenza
type: docs
weight: 50
url: /it/net/licensing/
description: Aspose. Diagram for .NET invita i suoi clienti a ottenere una licenza classica e una licenza a consumo. Oltre a utilizzare una licenza limitata per esplorare meglio il prodotto.
---
## **Valuta Aspose.Diagram**
È possibile scaricare facilmente il prodotto Aspose.Diagram for .NET a scopo di valutazione. Si prega di fare riferimento al[Aspose.Diagram for .NET pagina di download](https://www.nuget.org/packages/Aspose.Diagram/)per scoprire l'ultima versione. Il download di valutazione è lo stesso del download acquistato. La versione di valutazione diventa semplicemente concessa in licenza quando aggiungi alcune righe di codice per applicare la licenza.

La versione di valutazione di Aspose.Diagram (senza una licenza specificata) fornisce la piena funzionalità del prodotto, ma inserisce una filigrana di valutazione al centro del documento all'apertura e al salvataggio e limita la lettura solo delle prime dieci forme della prima pagina del tuo Visio diagram .

![cose da fare:immagine_alt_testo](licensing_1.png)
### **Limiti della versione di valutazione**
La versione di valutazione fornisce tutte le funzionalità tranne le seguenti:

- Puoi leggere solo le prime dieci forme della prima pagina di Visio diagram.
- You will also see evaluation watermark in exported images and PDF files.

{{% alert color="primary" %}} 

 Se vuoi provare Aspose.Diagram senza limiti di valutazione, richiedi una licenza temporanea di 30 giorni. Per favore riferisci a[Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) per maggiori informazioni.

{{% /alert %}} 
## **Applicazione di una licenza**
Una volta che sei soddisfatto del tuo[valutazione](https://downloads.aspose.com/diagram/net) di Aspose.Diagram for .NET, acquista una licenza al sito Aspose:[Portale acquisti](https://purchase.aspose.com/buy) . Prendi familiarità con i diversi tipi di licenza disponibili. Se hai qualche domanda,[contattare il team commerciale Aspose](https://about.aspose.com/contact) e saranno felici di aiutarti.

Ogni licenza Aspose comporta un abbonamento di un anno per aggiornamenti gratuiti a eventuali nuove versioni o correzioni che escono durante questo periodo. Forniamo supporto tecnico gratuito e illimitato sia agli utenti con licenza che a quelli di valutazione.

La licenza è un file XML di testo semplice che contiene dettagli come il nome del prodotto, il numero di sviluppatori con licenza, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificarlo: anche l'aggiunta di un'ulteriore interruzione di riga al file lo invalida.
### **Quando applicare una licenza**
Segui queste semplici regole:

- La licenza deve essere impostata una sola volta per dominio dell'applicazione.
- È necessario impostare la licenza prima di utilizzare qualsiasi altra classe Aspose.Diagram.
- Chiamare SetLicense più volte non è dannoso, ma fa perdere tempo al processore.
- Se stai sviluppando un'applicazione console o moduli Windows, chiama SetLicense nel codice di avvio, prima di utilizzare le classi Aspose.Diagram.
- Quando si sviluppa un'applicazione ASP.NET, chiamare SetLicense dal file Global.asax.cs, nel metodo protetto Aplication_Start. Viene chiamato una volta all'avvio dell'applicazione.
- Non chiamare SetLicense dall'interno dei metodi Page_Load poiché significa che la licenza verrà caricata ogni volta che viene caricata una pagina web.
- Se stai sviluppando una libreria di classi, chiami SetLicense da un costruttore statico della classe che utilizza Aspose.Diagram. Il costruttore statico viene eseguito prima che venga creata un'istanza della tua classe assicurandosi che la licenza Aspose.Diagram sia impostata correttamente.
### **Applica la licenza utilizzando l'oggetto File o Stream**
 Utilizzare il[Licenza.ImpostaLicenza](https://reference.aspose.com/diagram/net/aspose.diagram/license)metodo per concedere in licenza il componente. Il modo più semplice per impostare una licenza è inserire il file di licenza nella stessa cartella di Aspose.Diagram.dll e specificare il nome del file, senza un percorso, come mostrato di seguito.
#### **Caricamento di una licenza da file**
Questo frammento di codice inizializza una licenza memorizzata in un file o in una risorsa incorporata.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";

License license = new License();
license.SetLicense(dataDir + "Aspose.Diagram.lic");

{{< /highlight >}}

#### **Caricamento di una licenza da un oggetto flusso**
Questi frammenti di codice inizializzano la licenza dal flusso.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";
// Load an existing Visio file in the stream
FileStream LicStream = new FileStream(dataDir + "Aspose.Diagram.lic", FileMode.Open);

License license = new License();
license.SetLicense(LicStream);

{{< /highlight >}}

## **Applicare la licenza misurata**
Aspose.Diagram for .NET API consente agli sviluppatori di applicare la licenza misurata. È un nuovo meccanismo di licenza. Il nuovo meccanismo di licenza verrà utilizzato insieme al metodo di licenza esistente. I clienti che desiderano essere fatturati in base all'utilizzo delle funzionalità API possono utilizzare le licenze a consumo. Per maggiori dettagli, fare riferimento a[Domande frequenti sulle licenze misurate](https://purchase.aspose.com/faqs/licensing/metered)sezione.

Una nuova classe[Misurato](https://reference.aspose.com/diagram/net/aspose.diagram/metered)è stato aggiunto per applicare la chiave misurata. Questo esempio di codice mostra come impostare chiavi pubbliche e private misurate:


{{< highlight csharp >}}
// Initialize a Metered license class object
Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();
// apply public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}

