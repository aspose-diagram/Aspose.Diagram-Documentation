---
title: Aspose.Diagram Operazioni sui caratteri
type: docs
weight: 170
url: /it/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

Aspose.Diagram consente agli sviluppatori di impostare le directory dei font per il rendering nei diagrammi Visio. Questo articolo mostra come utilizzare i caratteri dalle directory personalizzate.

{{% /alert %}} 
### **Lavorare con i caratteri**
#### **Dove Aspose.Diagram cerca i caratteri TrueType su Windows**
 Aspose.Diagram cerca i caratteri nel file**Windows\Font** cartella. Questa impostazione predefinita funziona la maggior parte delle volte, quindi specifica le tue cartelle di caratteri solo se ne hai davvero bisogno.
#### **Come specificare in modo esplicito una cartella dei caratteri**
 Aspose.Diagram API ha esposto il metodo setFontDirs per il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class per specificare le cartelle dei caratteri come descritto di seguito.

1. Il metodo Diagram.setFontDirs accetta un array di stringhe come parametro, quindi lo sviluppatore può specificare molte directory di font utilizzando questo approccio.

{{% alert color="primary" %}} 

Quando si specifica la cartella dei caratteri utilizzando l'approccio sopra menzionato, si consiglia di impostare la posizione del carattere all'inizio dell'applicazione, altrimenti si potrebbero ricevere risultati con una formattazione scadente.

{{% /alert %}} {{% alert color="primary" %}} 

L'impostazione della cartella dei caratteri utilizzando uno dei metodi di cui sopra non garantisce che Aspose.Diagram API non cercherà i caratteri nelle posizioni predefinite come la cartella dei caratteri del sistema.

{{% /alert %}} 

Illustra come impostare Aspose.Diagram per cercare in più cartelle i caratteri TrueType durante il rendering o l'incorporamento dei caratteri.
#### **Esempio di programmazione**
L'esempio di codice seguente mostra come impostare Aspose.Diagram per cercare in più cartelle i caratteri TrueType durante il rendering o l'incorporamento dei caratteri.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Fonts-SpecifyFontLocation-SpecifyFontLocation.java" >}}
### **Ricevi notifica di caratteri mancanti e sostituzione di caratteri durante il rendering**
Aspose.Diagram API richiede l'accesso al carattere accurato per rendere correttamente il disegno in formato PDF. Se il font richiesto non è disponibile sulla macchina, Aspose.Diagram API esegue il rendering di qualsiasi istanza di quel font utilizzando il font predefinito o il font più vicino disponibile sulla macchina, poiché questa sostituzione può modificare l'aspetto del disegno renderizzato, gli sviluppatori potrebbero dover essere notificato quando manca un carattere e con quale carattere verrà sostituito.
#### **Notifica di caratteri mancanti e esempio di programmazione per la sostituzione dei caratteri**
Per essere avvisati della sostituzione del carattere durante il rendering:

1. Creare una classe che implementa il[AvvisoRichiamata](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. Passalo alla proprietà PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback).

Durante il salvataggio del disegno l'istanza di[AvvisoRichiamata](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)viene chiamato se ci sono potenziali problemi di fedeltà con il disegno. In questo caso, scegliamo di elaborare solo gli avvisi relativi alla sostituzione dei caratteri e di stampare l'avviso sullo schermo. L'esempio seguente mostra come ricevere notifiche di sostituzioni di caratteri utilizzando[AvvisoRichiamata](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementazione di IWarningCallback**
L'ultimo passaggio consiste nel creare la classe che implementa il file[AvvisoRichiamata](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)interfaccia. Questa classe stamperà tutti gli avvisi di sostituzione dei caratteri nella console. L'esempio seguente mostra come implementare IWarningCallback per ricevere una notifica di qualsiasi sostituzione di font durante il salvataggio del documento.



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
