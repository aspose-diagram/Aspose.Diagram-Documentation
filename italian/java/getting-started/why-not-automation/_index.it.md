---
title: Perché non Automazione
type: docs
weight: 70
url: /it/java/why-not-automation/
---
{{% alert color="primary" %}} 

Perché le API Aspose sono un'opzione molto migliore dell'automazione Microsoft Office?

Sono due le domande che sentiamo più spesso qui allo Aspose:

1. **I tuoi prodotti richiedono l'installazione di Microsoft Office per funzionare?** 
 La semplice risposta è no. Aspose API sono totalmente indipendenti e non sono affiliate, né autorizzate, sponsorizzate o altrimenti approvate da Microsoft Corporation.
1. **Perché dovremmo utilizzare i prodotti Aspose piuttosto che utilizzare l'automazione Microsoft Office?** 
 La risposta più breve che potremmo dare è che ci sono molte ragioni, la principale è che lo stesso Microsoft sconsiglia vivamente l'automazione Office dalle soluzioni software:[Considerazioni per l'automazione lato server di Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office).

Esistono diversi motivi per cui le API Aspose sono un'alternativa migliore all'automazione. Alcuni dei motivi principali sono:

- [Sicurezza](/diagram/it/java/why-not-automation/)
- [Stabilità](/diagram/it/java/why-not-automation/)
- [Scalabilità/Velocità](/diagram/it/java/why-not-automation/)
- [Prezzo](/diagram/it/java/why-not-automation/)
- [Caratteristiche](/diagram/it/java/why-not-automation/)

I punti chiave sono descritti di seguito. Inoltre, assicurati di visitare i collegamenti alla fine di questa sezione.

{{% /alert %}} 
### **Sicurezza**
 Quella che segue è una citazione diretta dall'articolo Microsoft sopra citato:*"Office Le applicazioni non sono mai state concepite per l'uso lato server e pertanto non prendono in considerazione i problemi di sicurezza che devono affrontare i componenti distribuiti. Office non autentica le richieste in arrivo e non ti protegge dall'esecuzione involontaria di macro o dall'avvio di un altro server che potrebbero eseguire macro, dal codice lato server. Non aprire file caricati sul server da un Web anonimo! In base alle ultime impostazioni di sicurezza impostate, il server può eseguire macro in un contesto di amministratore o di sistema con privilegi e compromettere la tua rete! Inoltre, Office utilizza molti componenti lato client (come Simple MAPI, WinInet e MSDAIPP) che possono memorizzare nella cache le informazioni di autenticazione del client per velocizzare l'elaborazione. Se Office viene automatizzato lato server, uno può servire più di un client e poiché le informazioni di autenticazione sono state memorizzate nella cache per quella sessione, è possibile che un client possa utilizzare la cache modificare le credenziali di un altro client e quindi ottenere autorizzazioni di accesso non concesse impersonando altri utenti."*

prodotti Aspose sono molto sicuri. Le API Aspose vengono eseguite nello stesso contesto utente di tutte le applicazioni .NET e Java. Pertanto, le API Aspose non rappresentano un potenziale rischio per le risorse vitali del sistema. Inoltre, quando un documento viene aperto da un Aspose API, le macro non vengono eseguite automaticamente. Le API Aspose sono state create con l'obiettivo di consentire agli sviluppatori di creare, manipolare e salvare i file Office. Nessuno dei rischi associati al pacchetto Microsoft Office è inerente alle API Aspose.
### **Stabilità**
 Quella che segue è una citazione diretta dall'articolo Microsoft sopra citato:*"Office 2000, Office XP e Office 2003 utilizzano la tecnologia Microsoft Windows Installer (MSI) per semplificare l'installazione e l'autoriparazione per l'utente finale. MSI introduce il concetto di "installazione al primo utilizzo", che consente l'installazione dinamica delle funzionalità o configurato in fase di esecuzione (per il sistema o più spesso per un particolare utente).In un ambiente lato server, ciò rallenta le prestazioni e aumenta la probabilità che venga visualizzata una finestra di dialogo che richiede all'utente di approvare l'installazione o fornire un disco di installazione appropriato. Sebbene sia progettato per aumentare la resilienza di Office come prodotto per l'utente finale, l'implementazione delle funzionalità MSI di Office è controproducente in un ambiente lato server. Inoltre, la stabilità di Office in generale non può essere garantita quando si esegue il server -side perché non è stato progettato o testato per questo tipo di utilizzo.Utilizzare Office come componente di servizio su un server di rete può ridurre la stabilità di quella macchina e come di conseguenza la tua rete nel suo insieme. Se si prevede di automatizzare Office lato server, tentare di isolare il programma su un computer dedicato che non può influire sulle funzioni critiche e che può essere riavviato secondo necessità."*

Poiché le API Aspose sono impacchettate in un'unica libreria, non sarà mai necessario installare parti o pezzi aggiuntivi per il loro funzionamento. Le API Aspose sono utilizzate da varie applicazioni e non esiste alcuna parte del codice API progettata per attendere una risposta umana. Le API Aspose sono state accuratamente testate. Aspose Le API sono utilizzate da aziende come IBM , Hilton , Reader's Digest, Bank of America e molte altre.
### **Scalabilità/Velocità**
 Quella che segue è una citazione diretta dall'articolo Microsoft sopra citato:*"I componenti lato server devono essere componenti COM altamente rientranti e multi-thread con sovraccarico minimo e velocità effettiva elevata per più client. Office Le applicazioni sono sotto quasi tutti gli aspetti esattamente l'opposto. Sono server di automazione basati su STA non rientranti che sono progettati per fornire funzionalità diverse ma ad alta intensità di risorse per un singolo client. Offrono poca scalabilità come soluzione lato server e hanno limiti fissi per elementi importanti, come la memoria, che non possono essere modificati tramite la configurazione. Ancora più importante, usano global risorse (come file mappati in memoria, componenti aggiuntivi o modelli globali e server di automazione condivisi), che possono limitare il numero di istanze che possono essere eseguite contemporaneamente e portare a race condition se sono configurate in un ambiente multi-client. pianificare di eseguire più di un'istanza di qualsiasi applicazione Office allo stesso tempo, è necessario prendere in considerazione il "pooling" o la serializzazione dell'accesso all'applicazione Office per evitare potenziali ntial deadlock o danneggiamento dei dati."*

Aspose Le API sono altamente scalabili e velocissime. le applicazioni Office non erano progettate per essere utilizzate contemporaneamente da centinaia e migliaia di utenti; tuttavia, le API Aspose sono progettate proprio per questo. Le nostre API sono una vera soluzione e funzionano in modo impeccabile sia su un singolo server che alimenta una singola applicazione sia su una web farm con bilanciamento del carico che alimenta un'applicazione a livello aziendale.
### **Prezzo**
 Quando un'applicazione utilizza l'automazione Microsoft Office, è necessario acquistare una copia di Microsoft Office per ogni macchina che esegue l'applicazione. Ci sono molte volte in cui un'applicazione potrebbe aver bisogno di creare o manipolare un file office, ma non richiede che l'utente abbia Office. Aspose offre una soluzione molto[conveniente](https://purchase.aspose.com/), royalty free, licenza di ridistribuzione che consentirà la distribuzione a un numero illimitato di utenti senza problemi di licenza.

Quando si creano applicazioni basate sul Web è importante sapere che i componenti di automazione Microsoft Office non sono prezzati né concessi in licenza per soluzioni lato server; pertanto, non esiste una buona soluzione di licenza per la distribuzione di applicazioni Web che utilizzano i componenti Microsoft Office. Aspose offre una soluzione molto conveniente anche per applicazioni basate su server.
### **Caratteristiche**
 I componenti Aspose forniscono tutto il necessario per la gestione dei file Office e molto altro ancora. Sono progettati con la filosofia di consentire agli sviluppatori di ottenere i massimi risultati con la minima quantità di lavoro. A differenza dell'automazione Office, i componenti Aspose forniscono molte funzioni potenti e che fanno risparmiare tempo. Per esempio,[Aspose.Diagram](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram) offre agli sviluppatori la possibilità di esportare da a**Tabella dati** o**Visualizzazione dati** direttamente in un file Excel.[Ogni componente](https://products.aspose.com/total) della famiglia Aspose offre il proprio set di funzionalità uniche e potenti.

La parte migliore dell'acquisto di una suite Aspose API o API è l'accesso ai nostri team di sviluppo. I nostri team di sviluppo si rendono conto che se c'è una funzionalità di cui la tua azienda ha bisogno, molto probabilmente ne avranno bisogno anche altre aziende. Sebbene non tutte le richieste di funzionalità possano essere aggiunte, i nostri team cercano di essere molto aperti e flessibili quando forniscono assistenza. Questa mentalità è ciò che ha aiutato le API Aspose a diventare potenti quanto loro. Se ci sono funzionalità aggiuntive di cui hai bisogno dagli oggetti di automazione Office, le tue possibilità di averle aggiunte sono molto, molto basse.
### **Conclusione**
{{% alert color="primary" %}} 

 Questo articolo ha trattato i punti chiave del motivo per cui le API Aspose sono una scelta migliore rispetto all'automazione Office. Tutte le diverse API Aspose offrono un rischio senza alcun obbligo[versione di valutazione](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). Ti invitiamo a sfruttare questa valutazione per vedere cosa può fare Aspose per le tue applicazioni.

Per ulteriori informazioni, consultare questo articolo su Internet:

- [Considerazioni per l'automazione lato server di Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office)

{{% /alert %}}
