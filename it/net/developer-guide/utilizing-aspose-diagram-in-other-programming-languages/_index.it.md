---
title: Utilizzo di Aspose.Diagram in altri linguaggi di programmazione
type: docs
weight: 120
url: /it/net/utilizing-aspose-diagram-in-other-programming-languages/
description: Questa pagina descrive come utilizzare Aspose.Diagram in altri linguaggi di programmazione.
---
## **Use Aspose.Diagram for .NET via COM Interop**
 Le informazioni in questo argomento si applicano agli scenari in cui gli sviluppatori richiedono l'utilizzo[Aspose.Diagram for .NET](/diagram/it/net/home/) via COM Interop in any supported language.
### **Utilizzo dell'interoperabilità COM**
Aspose.Diagram for .NET executes under the control of the .NET Framework and this is called managed code. The code written in all of the languages those runs outside the .NET Framework and it is called unmanaged code. Interaction between unmanaged code and Aspose.Diagram occurs via the .NET facility called COM Interop.

Aspose.Diagram objects are .NET objects, but when used via COM Interop, they appear as COM objects in your programming language. Therefore, it is best to make sure you know how to create and use COM objects in your programming language, before you start using [Aspose.Diagram for .NET](/diagram/it/net/home/).

- Nel mondo COM distinguiamo server COM e client COM. Il server COM ha memorizzato le classi COM mentre il client COM richiede al server COM le istanze delle classi, ovvero gli oggetti COM.
-  Il client COM o semplicemente l'applicazione client può conoscere qualcosa del contenuto della classe COM o essere totalmente all'oscuro dei suoi metodi e proprietà. Pertanto l'applicazione client può rilevare la struttura della classe COM durante la compilazione/costruzione o solo durante l'esecuzione. Il processo di "scoperta" è noto come vincolante e così abbiamo**legame anticipato** e**rilegatura tardiva**.
- in breve la classe COM è come una scatola nera e per lavorare con essa è necessaria la libreria dei tipi, questo file binario ha una descrizione dei metodi della classe COM, proprietà e qualsiasi linguaggio di alto livello che supporta il lavoro con gli oggetti COM spesso ha un'espressione di sintassi per l'aggiunta della libreria dei tipi, per esempio questo è[**#importare**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) allo C++.
- la libreria dei tipi viene utilizzata per l'associazione anticipata.
-  un oggetto COM può esporre i suoi metodi e le sue proprietà in due modi: tramite a**interfaccia di spedizione** (dispinterface) e nella sua**vtable** (tabella delle funzioni virtuali).
-  all'interno del**dispatch** , ogni metodo e proprietà è identificato da un membro univoco; questo membro è l'identificatore di invio della funzione (o**DispID**).
- **vtable** è solo un insieme di puntatori a funzioni supportate dall'interfaccia della classe COM.
-  un oggetto che espone i propri metodi tramite entrambe le interfacce supporta a**doppia interfaccia**.
- ci sono vantaggi per entrambi i tipi di rilegatura. L'associazione anticipata offre migliori prestazioni e controllo della sintassi in fase di compilazione. L'associazione tardiva è più vantaggiosa quando scrivi ai clienti che intendi essere***compatibile con le versioni future*** della tua classe COM. Con l'associazione tardiva, le informazioni della libreria dei tipi non sono "cablate" nel client, quindi puoi essere più sicuro che il tuo client possa lavorare con le versioni future della classe COM senza modifiche al codice.
-  il meccanismo di associazione tardiva ha un grande vantaggio: se il creatore della DLL COM decide di rilasciare una nuova versione, con un diverso layout dell'interfaccia delle funzioni, qualsiasi codice che chiama quei metodi non andrà in crash a meno che i metodi non siano più disponibili; anche se il**vtable**è diverso il late binding riesce a scoprire i nuovi DISPID ea chiamare i metodi appropriati.

 Ecco gli argomenti che alla fine dovrai padroneggiare:

- Utilizzo di oggetti COM nel tuo linguaggio di programmazione. Vedere la documentazione del linguaggio di programmazione e gli argomenti specifici del linguaggio più avanti in questa documentazione.
-  Utilizzo di oggetti COM esposti da .NET COM Interop. Vedere[Interoperabilità con codice non gestito](https://docs.microsoft.com/en-us/dotnet/framework/interop/) e[Esposizione dei componenti .NET Framework a COM](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com) in MSDN.
-  Aspose.Diagram documento oggetto modello. Vedere[Aspose.Diagram Guida del programmatore](https://docs.aspose.com/diagram/net/developer-guide/) e[API Riferimento](https://reference.aspose.com/diagram/net).
#### **Registrati Aspose.Diagram for .NET con COM Interop**
È necessario installare Aspose.Diagram for .NET e assicurarsi che sia registrato con COM Interop (assicurandosi che possa essere chiamato da codice non gestito).

Per registrare manualmente Aspose.Diagram for .NET per l'interoperabilità COM:

1.  Dal**Inizio** menù, selezionare**Tutti i programmi** , poi**Microsoft Visual Studio**, **Visual Studio Tools** e infine,**Visual Studio Command Prompt**. In alcuni sistemi operativi, è disponibile anche nel percorso: "C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64"
1.  Immettere il comando per registrare l'assieme:
   1. .NET Framework 2.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /codebase
   1. .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /codebase
   1. .NET Framework 4.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /codebase

{{% alert color="primary" %}} 

Prestare attenzione che /codebase è necessario solo se Aspose.Diagram.dll non è in GAC, l'utilizzo di questa opzione fa in modo che regasm metta il percorso per l'assembly nel registro.

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe è uno strumento incluso in .NET Framework SDK. Tutti gli strumenti SDK .NET Framework si trovano nella*\Microsoft .NET\Framevork\<Versione Framework>* directory, per esempio*C:\Windows\Microsoft .NET\Framework\v4.0.30319*. If you use Visual Studio .NET:
 Dal**Inizio** menù, selezionare**Programmi** , seguito da**Microsoft Visual Studio .NET** , poi**Visual Studio .NET Tools** e infine,**Visual Studio .NET 2003 Command Prompt**.
Esegue un prompt dei comandi con tutte le variabili di ambiente necessarie impostate.

{{% /alert %}} 
##### **ProgID**
ProgID sta per "identificatore programmatico". È il nome di una classe COM utilizzata per creare un oggetto. I ProgID sono costituiti dal nome della libreria "Aspose.Diagram" e dal nome della classe.
##### **Libreria dei tipi**
Se il tuo linguaggio di programmazione (ad esempio Visual Basic o Delphi) ti consente di fare riferimento a una libreria dei tipi COM, aggiungi un riferimento a Aspose.Diagram.tlb e visualizza tutte le classi, i metodi, le proprietà e le enumerazioni Aspose.Diagram for .NET nel tuo browser oggetti.

Per generare un file TLB:

- .NET Framework 2.0
 regasm "C:\Programmi\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Programmi\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.tlb" /codebase
- .NET Framework 3.5
 regasm "C:\Programmi\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Programmi\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.tlb" /codebase
- .NET Framework 4.0
regasm "C:\Programmi\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Programmi\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.tlb" /codebase
#### **Creazione di oggetti COM**
La creazione di un oggetto COM è simile alla creazione di un normale oggetto .NET. Una volta creato, puoi accedere ai metodi e alle proprietà dell'oggetto, come se fosse un oggetto COM.

Alcuni metodi dispongono di overload e verranno esposti dall'interoperabilità COM con l'aggiunta di un suffisso numerico, ad eccezione del primo metodo che rimane invariato. Ad esempio, gli overload del metodo Diagram.Save diventano Diagram.Save, Diagram.Save_2 e così via.

{{% alert color="primary" %}} 

 Per ulteriori informazioni, vedere gli articoli specifici della lingua più avanti in questa documentazione.

{{% /alert %}} 
## **Aspose.Diagram Risorse**
Di seguito sono riportati i collegamenti ad alcune risorse utili di cui potresti aver bisogno per svolgere le tue attività.
- [Aspose.Diagram for Java Documentazione in linea](https://docs.aspose.com/diagram/java/)
- [Aspose.Diagram for Node.js via Java Online Documentation](https://docs.aspose.com/diagram/nodejsjava/)
- [Aspose.Diagram for Python via Java Online Documentation](https://docs.aspose.com/diagram/pythonjava/)

##### **Creazione di un assieme wrapper**
Se è necessario utilizzare molte classi, metodi e proprietà Aspose.Diagram for .NET, prendere in considerazione la creazione di un assembly wrapper (utilizzando C# o qualsiasi altro linguaggio di programmazione .NET). Gli assembly wrapper consentono di evitare l'uso di Aspose.Diagram for .NET direttamente dal codice non gestito.

Un buon approccio consiste nello sviluppare un assembly .NET che fa riferimento a Aspose.Diagram for .NET e fa tutto il lavoro con esso ed espone solo un set minimo di classi e metodi al codice non gestito. La tua applicazione quindi dovrebbe funzionare solo con la tua libreria wrapper.

Reducing the number of classes and methods that you need to invoke via COM Interop simplifies the project. Using .NET classes via COM Interop often requires advanced skills. 
## **Crea un disegno vuoto Visio in PHP utilizzando l'interoperabilità COM**
### **Prerequisiti**
 Configura il tuo PHP per lavorare con COM. Vedere<http://www.php.net/manual/en/ref.com.php> . Per ulteriori informazioni, consultare l'articolo denominato[Use Aspose.Diagram for .NET via COM Interop](/diagram/it/net/home/).
### **Creazione di un disegno vuoto Visio**
 Questa è una semplice applicazione che mostra come creare un disegno Visio vuoto utilizzando[Aspose.Diagram for .NET](/diagram/it/net/home/) in PHP via COM Interop.

**PHP**

{{< highlight "csharp" >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
