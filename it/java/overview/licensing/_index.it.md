---
title: Licenza
type: docs
weight: 60
url: /it/java/licensing/
---
## **Limiti della versione di valutazione**
 Una versione di valutazione gratuita di Aspose.Diagram for Java può essere scaricata da[Aspose Archivio](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **Limitazione**
La versione di valutazione fornisce tutte le funzionalità tranne le seguenti:

- Puoi leggere solo le prime dieci forme della prima pagina del tuo file VSD.
- You will also see evaluation watermark in exoprted images and PDF files.

 Se vuoi provare Aspose.Diagram senza limiti di valutazione, richiedi una licenza temporanea di 30 giorni. Per favore riferisci a[Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) per maggiori informazioni.
## **Applicazione di una licenza**
 È possibile scaricare una versione di valutazione di**Aspose.Diagram** for Java da[Aspose Archivio](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). La versione di valutazione offre assolutamente le stesse funzionalità della versione con licenza del prodotto. Inoltre, la versione di valutazione diventa semplicemente concessa in licenza quando acquisti una licenza e aggiungi un paio di righe di codice per applicare la licenza.

 Una volta che sei soddisfatto della tua valutazione di**Aspose.Diagram** , puoi[acquistare una licenza](https://purchase.aspose.com/buy) sul sito Aspose. Acquisisci familiarità con i diversi tipi di abbonamento offerti. In caso di domande, non esitare a contattare il team di vendita Aspose.

Ogni licenza Aspose comporta un abbonamento di un anno per aggiornamenti gratuiti a eventuali nuove versioni o correzioni che escono durante questo periodo. Il supporto tecnico è gratuito e illimitato e viene fornito sia agli utenti con licenza che a quelli di valutazione.

{{% alert color="primary" %}} 

 Se vuoi fare una prova**Aspose.Diagram** senza limitazioni della versione di valutazione, richiedi una licenza temporanea di 30 giorni. Per favore riferisci a[Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) per maggiori informazioni.

{{% /alert %}} 
### **Impostazione di una licenza**
La licenza è un file XML di testo semplice che contiene dettagli come il nome del prodotto, il numero di sviluppatori a cui è concesso in licenza, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificare il file; anche l'aggiunta involontaria di un'ulteriore interruzione di riga nel file lo invaliderà.

È necessario applicare una licenza prima di eseguire qualsiasi operazione con i documenti. Assicurati di farlo prima di creare un oggetto Diagram. È necessario impostare una licenza solo una volta per applicazione o processo.

La licenza può essere caricata da un flusso o da un file nelle seguenti posizioni:

1. Percorso esplicito.
1. La cartella che contiene Aspose.Diagram.jar.

 Utilizzare il[Licenza.impostaLicenza()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License) metodo per concedere in licenza il componente. Spesso il modo più semplice per impostare una licenza consiste nell'inserire il file di licenza nella stessa cartella di Aspose.Diagram.jar e specificare solo il nome del file senza percorso, come mostrato nell'esempio seguente:
#### **Esempio 1**
 In questo esempio**Aspose.Diagram** tenterà di trovare il file di licenza nella cartella che contiene i JAR della tua applicazione.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **Esempio 2**
Inizializza una licenza da un flusso.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **Convalida la licenza**
 È possibile verificare se la licenza è stata impostata correttamente o meno. Il[Licenza](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)class ha il campo isLicensed che restituirà true se la licenza è stata impostata correttamente.

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Applicare la licenza misurata**
Aspose.Diagram for Java API consente agli sviluppatori di applicare la licenza misurata. È un nuovo meccanismo di licenza. Il nuovo meccanismo di licenza verrà utilizzato insieme al metodo di licenza esistente. I clienti che desiderano essere fatturati in base all'utilizzo delle funzionalità API possono utilizzare le licenze a consumo. Per maggiori dettagli, fare riferimento a[Domande frequenti sulle licenze misurate](https://purchase.aspose.com/faqs/licensing/metered)sezione.

Una nuova classe[Misurato](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered) è stato aggiunto per applicare la chiave misurata. Questo esempio di codice mostra come impostare chiavi pubbliche e private misurate:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// Initialize a Metered license class object
Metered metered = new Metered();
// apply public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```
