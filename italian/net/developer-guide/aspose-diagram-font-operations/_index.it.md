---
title: Aspose.Diagram Operazioni sui caratteri
type: docs
weight: 180
url: /it/net/aspose-diagram-font-operations/
description: Questa pagina descrive come manipolare i font con la libreria Aspose.Diagram.
---
## **Come specificare la posizione dei caratteri TrueType**
Aspose.Diagram consente agli sviluppatori di impostare le directory dei font per il rendering nei diagrammi Visio. Questo articolo mostra come utilizzare i caratteri dalle directory personalizzate.
### **Lavorare con i caratteri**
#### **Dove Aspose.Diagram cerca i caratteri TrueType su Windows**
 Aspose.Diagram cerca i caratteri nel file**Windows\Font** cartella. Questa impostazione predefinita funziona la maggior parte delle volte, quindi specifica le tue cartelle di caratteri solo se ne hai davvero bisogno.
#### **Come specificare in modo esplicito una cartella dei caratteri**
Aspose.Diagram API ha esposto la proprietà FontDirs per il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class per specificare le cartelle dei caratteri come descritto di seguito.

1. La proprietà Diagram.FontDirs accetta una matrice di stringhe in modo che lo sviluppatore possa specificare molte directory di caratteri utilizzando questo approccio.

{{% alert color="primary" %}} 

Quando si specifica la cartella dei caratteri utilizzando l'approccio sopra menzionato, si consiglia di impostare la posizione del carattere all'inizio dell'applicazione, altrimenti si potrebbero ricevere risultati con una formattazione scadente.

{{% /alert %}} {{% alert color="primary" %}} 

L'impostazione della cartella dei caratteri utilizzando uno dei metodi di cui sopra non garantisce che Aspose.Diagram API non cercherà i caratteri nelle posizioni predefinite come la cartella dei caratteri del sistema.

{{% /alert %}} 
#### **Esempio di programmazione**
L'esempio di codice seguente mostra come impostare Aspose.Diagram per cercare in più cartelle i caratteri TrueType durante il rendering o l'incorporamento dei caratteri.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SpecifyFontLocation-SpecifyFontLocation.cs" >}}
### **Ricevi notifica di caratteri mancanti e sostituzione di caratteri durante il rendering**
Aspose.Diagram API richiede l'accesso al carattere accurato per rendere correttamente il disegno in formato PDF. Se il font richiesto non è disponibile sulla macchina, Aspose.Diagram API esegue il rendering di qualsiasi istanza di quel font utilizzando il font predefinito o il font più vicino disponibile sulla macchina, poiché questa sostituzione può modificare l'aspetto del disegno renderizzato, gli sviluppatori potrebbero dover essere notificato quando manca un carattere e con quale carattere verrà sostituito.
#### **Notifica di caratteri mancanti e esempio di programmazione per la sostituzione dei caratteri**
Per essere avvisati della sostituzione del carattere durante il rendering:

1. Creare una classe che implementa il[AvvisoRichiamata](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)
1. Passalo alla proprietà PdfSaveOptions.WarningCallback.

Durante il salvataggio del disegno l'istanza di[AvvisoRichiamata](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)viene chiamato se ci sono potenziali problemi di fedeltà con il disegno. In questo caso, scegliamo di elaborare solo gli avvisi relativi alla sostituzione dei caratteri e di stampare l'avviso sullo schermo. L'esempio seguente mostra come ricevere notifiche di sostituzioni di caratteri utilizzando[AvvisoRichiamata](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback).

**C#**

{{< highlight "java" >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementazione di IWarningCallback**
L'ultimo passaggio consiste nel creare la classe che implementa il file[AvvisoRichiamata](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)interfaccia. Questa classe stamperà tutti gli avvisi di sostituzione dei caratteri nella console. L'esempio seguente mostra come implementare IWarningCallback per ricevere una notifica di qualsiasi sostituzione di font durante il salvataggio del documento.

**C#**

{{< highlight "java" >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
