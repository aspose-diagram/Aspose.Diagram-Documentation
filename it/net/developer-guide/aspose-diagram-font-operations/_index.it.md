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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

String[] fontDirs = new String[] { "C:\\MyFonts\\", "D:\\Misc\\Fonts\\" };
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Setting the custom font directories
diagram.FontDirs = fontDirs;

// Saving Visio diagram in PDF format
diagram.Save(dataDir + "SpecifyFontLocation_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```
### **Ricevi notifica di caratteri mancanti e sostituzione di caratteri durante il rendering**
Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.
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
