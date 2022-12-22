---
title: Perché non l'automazione
type: docs
weight: 40
url: /it/net/why-not-automation/
description: Questa pagina descrive perché non l'automazione.
---
{{% alert color="primary" %}} 

Perché i componenti Aspose sono un'opzione molto migliore dell'automazione Microsoft Office?*

Sono due le domande che sentiamo più spesso qui allo Aspose:

1. **I tuoi prodotti richiedono l'installazione di Microsoft Office per funzionare?** 
La semplice risposta è no. I componenti Aspose sono totalmente indipendenti e non sono affiliati, né autorizzati, sponsorizzati o altrimenti approvati da Microsoft Corporation.
1. **Perché dovremmo utilizzare i prodotti Aspose piuttosto che utilizzare l'automazione Microsoft Office?** 
 La risposta più breve che potremmo dare è che ci sono molte ragioni, la principale è che lo stesso Microsoft sconsiglia vivamente l'automazione Office dalle soluzioni software:[Considerazioni per l'automazione lato server di Office](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q257757).

{{% /alert %}} 
## **Perché non l'automazione**
Ci sono diversi motivi per cui i componenti Aspose sono una migliore alternativa all'automazione. Alcuni dei punti chiave sono descritti di seguito. Inoltre, assicurati di visitare i collegamenti alla fine di questa sezione.
### **Sicurezza**
Quella che segue è una citazione diretta dall'articolo Microsoft sopra citato:

*"Office Le applicazioni non sono mai state concepite per l'uso lato server e pertanto non prendono in considerazione i problemi di sicurezza che devono affrontare i componenti distribuiti. Office non autentica le richieste in arrivo e non ti protegge dall'esecuzione involontaria di macro o dall'avvio di un altro server che potrebbero eseguire macro, dal codice lato server. Non aprire file caricati sul server da un Web anonimo! In base alle ultime impostazioni di sicurezza impostate, il server può eseguire macro in un contesto di amministratore o di sistema con privilegi e compromettere la tua rete! Inoltre, Office utilizza molti componenti lato client (come Simple MAPI, WinInet e MSDAIPP) che possono memorizzare nella cache le informazioni di autenticazione del client per velocizzare l'elaborazione. Se Office viene automatizzato lato server, uno può servire più di un client e poiché le informazioni di autenticazione sono state memorizzate nella cache per quella sessione, è possibile che un client possa utilizzare la cache modificare le credenziali di un altro client e quindi ottenere autorizzazioni di accesso non concesse impersonando altri utenti."*

I prodotti Aspose sono molto sicuri. I componenti Aspose vengono eseguiti nello stesso contesto utente di tutte le applicazioni ASP.NET, sotto l'utente ASPNET. Pertanto, i componenti Aspose non rappresentano un potenziale rischio per le risorse vitali del sistema. Inoltre, quando un documento viene aperto da un componente Aspose, le macro non vengono eseguite automaticamente. I componenti Aspose sono stati creati con l'obiettivo di consentire agli sviluppatori di creare, manipolare e salvare i file Office. Nessuno dei rischi associati al pacchetto Microsoft Office è inerente ai componenti Aspose.
### **Stabilità**
Quella che segue è una citazione diretta dall'articolo Microsoft sopra citato:

*"Office 2000, Office XP e Office 2003 utilizzano la tecnologia Microsoft Windows Installer (MSI) per semplificare l'installazione e l'autoriparazione per l'utente finale. MSI introduce il concetto di "installazione al primo utilizzo", che consente l'installazione dinamica delle funzionalità o configurato in fase di esecuzione (per il sistema o più spesso per un particolare utente).In un ambiente lato server, ciò rallenta le prestazioni e aumenta la probabilità che venga visualizzata una finestra di dialogo che richiede all'utente di approvare l'installazione o fornire un disco di installazione appropriato. Sebbene sia progettato per aumentare la resilienza di Office come prodotto per l'utente finale, l'implementazione delle funzionalità MSI di Office è controproducente in un ambiente lato server. Inoltre, la stabilità di Office in generale non può essere garantita quando viene eseguito il server -side perché non è stato progettato o testato per questo tipo di utilizzo.Utilizzare Office come componente di servizio su un server di rete può ridurre la stabilità di quella macchina e come di conseguenza la tua rete nel suo insieme. Se si prevede di automatizzare Office lato server, tentare di isolare il programma su un computer dedicato che non può influire sulle funzioni critiche e che può essere riavviato secondo necessità."*

Poiché i componenti Aspose sono impacchettati in una singola DLL, non sarà mai necessario installare parti o pezzi aggiuntivi per il loro funzionamento. I componenti Aspose sono utilizzati solo dalle applicazioni .NET e non vi è alcuna parte del codice del componente progettata per attendere una risposta umana. Aspose i componenti sono stati accuratamente testati. I componenti Aspose sono utilizzati da aziende come IBM, Hilton, Reader's Digest, Bank of America e molte altre.
### **Scalabilità/Velocità**
Quella che segue è una citazione diretta dall'articolo Microsoft sopra citato:

*"I componenti lato server devono essere componenti COM altamente rientranti e multi-thread con sovraccarico minimo e velocità effettiva elevata per più client. Office Le applicazioni sono sotto quasi tutti gli aspetti esattamente l'opposto. Sono server di automazione basati su STA non rientranti che sono progettati per fornire funzionalità diverse ma ad alta intensità di risorse per un singolo client. Offrono poca scalabilità come soluzione lato server e hanno limiti fissi per elementi importanti, come la memoria, che non possono essere modificati tramite la configurazione. Ancora più importante, usano global risorse (come file mappati in memoria, componenti aggiuntivi o modelli globali e server di automazione condivisi), che possono limitare il numero di istanze che possono essere eseguite contemporaneamente e portare a race condition se sono configurate in un ambiente multi-client. pianificare di eseguire più di un'istanza di qualsiasi applicazione Office allo stesso tempo, è necessario prendere in considerazione il "pooling" o la serializzazione dell'accesso all'applicazione Office per evitare potenziali ntial deadlock o danneggiamento dei dati."*

Aspose sono altamente scalabili e velocissimi. le applicazioni Office non erano progettate per essere utilizzate contemporaneamente da centinaia e migliaia di utenti; tuttavia, i componenti Aspose sono progettati proprio per questo. I nostri componenti sono una vera soluzione .NET e funzionano in modo impeccabile sia su un singolo server che alimenta una singola applicazione sia su una web farm con bilanciamento del carico che alimenta un'applicazione a livello aziendale.
### **Prezzo**
 Quando un'applicazione utilizza l'automazione Microsoft Office, è necessario acquistare una copia di Microsoft Office per ogni macchina che esegue l'applicazione. Ci sono molte volte in cui un'applicazione potrebbe aver bisogno di creare o manipolare un file office, ma non richiede che l'utente abbia Office. Aspose offre una soluzione molto[conveniente](https://purchase.aspose.com/buy), royalty free, licenza di ridistribuzione che consentirà la distribuzione a un numero illimitato di utenti senza problemi di licenza.

Quando si creano applicazioni basate sul Web, è importante sapere che i componenti di automazione Microsoft Office non sono prezzati né concessi in licenza per soluzioni lato server ([Licenza dei componenti Web Office 2000 e delle estensioni del server Office](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q243006)); pertanto, non esiste una buona soluzione di licenza per la distribuzione di applicazioni Web che utilizzano i componenti Microsoft Office. Aspose offre una soluzione molto conveniente anche per applicazioni basate su server.
### **Caratteristiche**
 I componenti Aspose forniscono tutto il necessario per la gestione dei file Office e molto altro ancora. Sono progettati con la filosofia di consentire agli sviluppatori di ottenere i massimi risultati con la minima quantità di lavoro. A differenza dell'automazione Office, i componenti Aspose forniscono molte funzioni potenti e che fanno risparmiare tempo. Per esempio,[Aspose.Diagram](https://products.aspose.com/diagram/net/) offre agli sviluppatori la possibilità di creare, leggere, scrivere, esportare, stampare, accedere e proteggere Visio diagram e anche le sue forme.[Ogni componente](https://products.aspose.com/total/) della famiglia Aspose offre il proprio set di funzionalità uniche e potenti.

La parte migliore dell'acquisto di un componente Aspose o di una suite di componenti è l'accesso ai nostri team di sviluppo. I nostri team di sviluppo si rendono conto che se c'è una funzionalità di cui la tua azienda ha bisogno, molto probabilmente ne avranno bisogno anche altre aziende. Sebbene non tutte le richieste di funzionalità possano essere aggiunte, i nostri team cercano di essere molto aperti e flessibili quando forniscono assistenza. Questa mentalità è ciò che ha aiutato i componenti Aspose a diventare potenti quanto loro. Se ci sono funzionalità aggiuntive di cui hai bisogno dagli oggetti di automazione Office, le tue possibilità di averle aggiunte sono molto, molto basse.
### **Conclusione**
{{% alert color="primary" %}} 

 Sebbene questo articolo abbia trattato molti dei punti chiave per cui i componenti Aspose sono una scelta migliore rispetto all'automazione Office, ce ne sono molti, molti altri. Questo articolo affronta principalmente solo i punti più importanti. Tutti i diversi componenti Aspose offrono un rischio gratuito, nessun obbligo[Versione di valutazione](https://www.nuget.org/packages/Aspose.Diagram/)Ti invitiamo ad approfittare di tale valutazione per vedere meglio cosa può fare Aspose per le tue applicazioni.

{{% /alert %}}
