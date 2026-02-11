---
title: Creare, aggiornare, disporre e adattare automaticamente le forme
type: docs
weight: 10
url: /it/net/create-update-layout-and-auto-fit-shapes/
description: Usa C# Diagram API per creare, aggiornare e creare forme di layout automatico nei file Visio utilizzando C# all'interno delle tue applicazioni. Guida completa con esempi di codice C#.
---
## **Creazione di un numero Diagram**
 Aspose.Diagram for .NET consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un numero diagram. Quindi[aggiungere forme e connettori](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)per creare diagram. Utilizzare il costruttore predefinito di[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class per creare un nuovo diagram.
### **Esempio di programmazione**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Forme di layout in stile diagramma di flusso**
 Con alcuni tipi di disegni collegati, come diagrammi di flusso e diagrammi di rete, è possibile utilizzare il file**Forme di layout** funzione per posizionare automaticamente le forme. Il posizionamento automatico è più rapido rispetto al trascinamento manuale di ciascuna forma in una nuova posizione.

Ad esempio, se stai aggiornando un diagramma di flusso di grandi dimensioni per includere un nuovo processo, puoi aggiungere e connettere le forme che compongono il processo e quindi utilizzare la funzionalità di layout per disporre automaticamente il disegno aggiornato.

 Il metodo Layout, esposto da[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class impagina le forme e/o reindirizza i connettori su tutte le pagine di diagram. Questo metodo accetta un file[LayoutOptions](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)oggetto come argomento. Usare le diverse proprietà esposte dalla classe LayoutOptions per disporre automaticamente le forme.

L'immagine seguente mostra lo diagram caricato dai frammenti di codice in questo articolo, prima che venga applicato il layout automatico. I frammenti di codice mostrano come fare domanda[layout del diagramma di flusso](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) e[layout ad albero compatto](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**La fonte diagram.**

![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_1.png)

I frammenti di codice in questo articolo prendono il codice sorgente diagram e vi applicano diversi tipi di layout automatico, salvandoli ciascuno in un file separato.

|<p>**Layout delle forme dal basso verso l'alto** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layout delle forme dall'alto verso il basso** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Forme di layout da sinistra a destra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layout delle forme da destra a sinistra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Per disporre le forme in stile diagramma di flusso:

1. Creare un'istanza della classe Diagram.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà correlate allo stile del diagramma di flusso.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il disegno Visio.
### **Esempio di programmazione in stile diagramma di flusso**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **Disposizione delle forme nello stile ad albero compatto**
 Lo stile di layout ad albero compatto cerca di costruire una struttura ad albero. Utilizza lo stesso file di input del file[esempio sopra](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) salva in diversi stili di alberi compatti diversi.

|<p>**Layout ad albero compatto - in basso ea destra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Layout ad albero compatto - in basso ea sinistra** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Layout ad albero compatto - a destra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Layout ad albero compatto - a sinistra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Per disporre le forme nello stile ad albero compatto:

1.  Crea un'istanza di[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà dello stile dell'albero compatto.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il file Visio.
#### **Esempio di programmazione in stile albero compatto**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Adatta automaticamente il Visio Diagram**
 Aspose.Diagram API supporta l'autoadattamento del disegno Visio. Questa operazione di funzionalità aiuta a portare le forme esterne all'interno del limite di pagina Visio. Aspose.Diagram for .NET API ha il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class che rappresenta un disegno Visio. Il[DiagramSaveOptions](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) espone la proprietà AutoFitPageToDrawingContent per adattare automaticamente il disegno Visio.

Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Crea un oggetto della classe DiagramSaveOptions e passa il formato di file risultante.
1. Impostare la proprietà AutoFitPageToDrawingContent dell'oggetto DiagramSaveOptions.
1. Chiama il metodo Save dell'oggetto classe Diagram e passa anche il percorso file completo e l'oggetto DiagramSaveOptions.
### **Esempio di programmazione dell'adattamento automatico**
Il codice di esempio seguente mostra come adattare automaticamente le forme nel Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}
```
## **Lavorare con il progetto VBA**
### **Modifica il codice del modulo VBA in Visio Diagram**
 Questo articolo mostra come modificare automaticamente il codice di un modulo VBA utilizzando Aspose.Diagram for .NET. Abbiamo aggiunto[Modulo Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) e[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) classi. Queste classi aiutano a ottenere il controllo sul progetto VBA. Gli sviluppatori possono estrarre e modificare il codice del modulo VBA.
### **Modifica l'esempio di programmazione del codice del modulo VBA**
Si prega di controllare questo esempio di codice:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **Rimuovi tutte le macro da Visio Diagram**
 Aspose.Diagram for .NET consente agli sviluppatori di rimuovere tutte le macro da Visio diagram. La proprietà VbProjectData, esposta dal[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, permette di rimuovere tutte le macro dal disegno Visio.
### **Esempio di programmazione Rimuovi tutte le macro**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Creazione di un nuovo Diagram con VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)consente agli sviluppatori di creare e lavorare con diagrammi Microsoft Office Visio e incorporare funzionalità nelle loro applicazioni software. Esistono altri modi per lavorare con i file Visio, più comunemente, Microsoft Automation. Sfortunatamente, questo ha alcune limitazioni. Aspose.Diagram è potente e veloce e funziona in modo indipendente senza Microsoft Office installazione.

 Questo articolo sulla migrazione mostra come utilizzare first[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) poi[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) per creare un nuovo diagram e aggiungervi alcune forme. Noterai che il codice Aspose.Diagram è più corto del codice VSTO. Sentiti libero di utilizzare il codice come base per il tuo sviluppo e di migliorarlo per soddisfare le tue esigenze. VSTO ti consente di programmare con file Microsoft Visio. Per creare un nuovo diagram:

1. Creare un oggetto applicazione Visio.
1. Rendi invisibile l'oggetto dell'applicazione.
1. Crea un diagram vuoto.
1. Aggiungi forme da Visio maestri (stencil).
1. Salva il file come VDX.
### **Crea nuovo Diagram con esempio di programmazione VSTO**
{{% alert color="primary" %}}

utilizzando Visio = Microsoft.Office.Interop.Visio;
Importazioni Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Esempio:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}
```
## **Creazione di un nuovo Diagram con Aspose.Diagram for .NET**
Utilizzando Aspose.Diagram API, gli sviluppatori non hanno bisogno dell'installazione Microsoft Office Visio sulla macchina e possono lavorare indipendentemente dall'automazione Microsoft Office.

Per creare un nuovo diagram:

1. Crea un diagram vuoto.
1. Aggiungi forme da Visio maestri (stencil).
1. Salva il file come VDX.
### **Nuovo Diagram con Aspose.Diagram for .NET Esempio di programmazione**
{{% alert color="primary" %}}

utilizzando il numero Aspose.Diagram;
Importazioni Aspose.Diagram

{{% /alert %}}

Esempio:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Aggiorna proprietà forma**
 Quando si lavora con i diagrammi Microsoft Visio, gli utenti possono aggiornare gli attributi della forma inclusi testo, stile, posizione, altezza e larghezza. Come sviluppatore di software che lavora con i file Visio, ti verrà chiesto di farlo a livello di codice. La buona notizia è che è possibile, sia utilizzando i meccanismi di programmazione con i file Visio forniti da Microsoft, VSTO, sia utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Sotto argomento mostra come utilizzare[VSTO](https://products.aspose.com/diagram/net/) e[Aspose.Diagram](https://products.aspose.com/diagram/net/) per aggiornare le proprietà della forma. I frammenti di codice seguenti mostrano come aggiornare le proprietà della forma per VSTO e Aspose.Diagram for .NET. Sentiti libero di usare il codice e applicarlo alla tua situazione particolare.
### **Aggiornamento delle proprietà della forma con VSTO**
VSTO ti consente di programmare con file Microsoft Visio. Per aggiornare le proprietà della forma:

1. Creare un oggetto applicazione Visio.
1. Rendi invisibile l'oggetto dell'applicazione.
1. Apri un file Visio VSD esistente.
1. Trova la forma richiesta.
1. Aggiorna le proprietà della forma (testo, stile del testo, posizione e dimensione).
1. Salva il file come VDX.
#### **Aggiornamento delle proprietà della forma con l'esempio di programmazione VSTO**
{{% alert color="primary" %}}

utilizzando Visio = Microsoft.Office.Interop.Visio;
Importazioni Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Esempio:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}
```
### **Aggiornamento delle proprietà della forma con Aspose.Diagram for .NET**
Utilizzando Aspose.Diagram API, gli sviluppatori non hanno bisogno di Microsoft Office Visio sulla macchina e possono lavorare indipendentemente dall'automazione Microsoft Office.

Per aggiornare le proprietà della forma con Aspose.Diagram for .NET:

1. Apri un file Visio VSD esistente.
1. Trova la forma richiesta.
1. Aggiorna le proprietà della forma (testo, stile del testo, posizione e dimensione).
1. Salva il file come VDX.
#### **Aggiornamento delle proprietà della forma con l'esempio di programmazione Aspose.Diagram for .NET**
{{% alert color="primary" %}}

utilizzando il numero Aspose.Diagram;
Importazioni Aspose.Diagram

{{% /alert %}}

**Esempio:**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}
```
