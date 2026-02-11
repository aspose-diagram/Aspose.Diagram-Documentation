---
title: Creazione, layout e adattamento automatico delle forme
type: docs
weight: 10
url: /it/java/create-layout-and-auto-fit-shapes/
---
## **Creazione di un numero Diagram**
 Aspose.Diagram for Java consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un numero diagram. Quindi[aggiungere forme e connettori](/diagram/it/java/add-and-connect-visio-shapes/)per creare diagram. Utilizzare il costruttore predefinito di[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class per creare un nuovo diagram.
### **Esempio di programmazione**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Forme di layout in stile diagramma di flusso**
 Con alcuni tipi di disegni collegati, come diagrammi di flusso e diagrammi di rete, è possibile utilizzare il file**Forme di layout** funzione per posizionare automaticamente le forme. Il posizionamento automatico è più rapido rispetto al trascinamento manuale di ciascuna forma in una nuova posizione.

Ad esempio, se stai aggiornando un diagramma di flusso di grandi dimensioni per includere un nuovo processo, puoi aggiungere e connettere le forme che compongono il processo e quindi utilizzare la funzionalità di layout per disporre automaticamente il disegno aggiornato.

 Il metodo Layout, esposto da[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class impagina le forme e/o reindirizza i connettori su tutte le pagine di diagram. Questo metodo accetta un oggetto LayoutOptions come argomento. Usare le diverse proprietà esposte dalla classe LayoutOptions per disporre automaticamente le forme.

L'immagine seguente mostra lo diagram caricato dai frammenti di codice in questo articolo, prima che venga applicato il layout automatico. I frammenti di codice mostrano come fare domanda[layout del diagramma di flusso](/diagram/it/java/create-2c-layout-and-auto-fit-shapes/) e[layout ad albero compatto](/diagram/it/java/create-2c-layout-and-auto-fit-shapes/).

**La fonte diagram.** 

![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_1.png)

I frammenti di codice in questo articolo prendono il codice sorgente diagram e vi applicano diversi tipi di layout automatico, salvandoli ciascuno in un file separato.

|<p>**Layout delle forme dal basso verso l'alto** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layout delle forme dall'alto verso il basso** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Forme di layout da sinistra a destra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layout delle forme da destra a sinistra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_5.png)</p>|
Per disporre le forme in stile diagramma di flusso:

1. Creare un'istanza della classe Diagram.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà correlate allo stile del diagramma di flusso.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il disegno Visio.
### **Esempio di programmazione in stile diagramma di flusso**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInFlowchartStyle.class);     

// load an existing Visio diagram
String fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setSpaceShapes(1f);
flowChartOptions.setEnlargePage(true);

// set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_btm_top.vdx", SaveFileFormat.VDX);

// set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_top_btm.vdx", SaveFileFormat.VDX);

// set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_left_right.vdx", SaveFileFormat.VDX);

// set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_right_left.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **Disposizione delle forme nello stile ad albero compatto**
 Lo stile di layout ad albero compatto cerca di costruire una struttura ad albero. Utilizza lo stesso file di input del file[esempio sopra](/diagram/it/java/create-2c-layout-and-auto-fit-shapes/) salva in diversi stili di alberi compatti diversi.

|<p>**Layout ad albero compatto - in basso ea destra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Layout ad albero compatto - in basso ea sinistra** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Layout ad albero compatto - a destra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Layout ad albero compatto - a sinistra e in basso** </p><p>![cose da fare:immagine_alt_testo](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Per disporre le forme nello stile ad albero compatto:

1.  Crea un'istanza di[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) classe.
1. Creare un'istanza della classe LayoutOptions e impostare le proprietà dello stile dell'albero compatto.
1. Chiamare il metodo Layout della classe Diagram passando LayoutOptions.
1. Chiama il metodo Save della classe Diagram per scrivere il file Visio.
#### **Esempio di programmazione in stile albero compatto**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInCompactTreeStyle.class);
        
String fileName = "LayOutShapesInCompactTreeStyle.vdx";
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setEnlargePage(true);

// set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Adatta automaticamente il Visio Diagram**
Aspose.Diagram API supporta l'autoadattamento del disegno Visio. Questa operazione di funzionalità aiuta a portare le forme esterne all'interno del limite di pagina Visio.

Aspose.Diagram for Java API ha la classe Diagram che rappresenta un disegno Visio. La classe DiagramSaveOptions espone la proprietà AutoFitPageToDrawingContent per adattare automaticamente il disegno Visio.

Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Crea un oggetto della classe DiagramSaveOptions e passa il formato di file risultante.
1. Impostare la proprietà AutoFitPageToDrawingContent dell'oggetto DiagramSaveOptions.
1. Chiama il metodo Save dell'oggetto classe Diagram e passa anche il percorso file completo e l'oggetto DiagramSaveOptions.
### **Esempio di programmazione dell'adattamento automatico**
Il codice di esempio seguente mostra come adattare automaticamente le forme nel Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AutoFitShapesInVisio.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// set Auto fit page property
options.setAutoFitPageToDrawingContent(true);

// save Visio diagram
diagram.save(dataDir + "AutoFitShapesInVisio_Out.vsdx", options);

{{< /highlight >}}
```
## **Lavorare con il progetto VBA**
### **Modifica il codice del modulo VBA in Visio Diagram**
Questo articolo mostra come modificare automaticamente il codice di un modulo VBA utilizzando Aspose.Diagram for Java.

Abbiamo aggiunto le classi VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference e VbaProjectReferenceCollection. Queste classi aiutano a ottenere il controllo sul progetto VBA. Gli sviluppatori possono estrarre e modificare il codice del modulo VBA.
### **Modifica l'esempio di programmazione del codice del modulo VBA**
Si prega di controllare questo esempio di codice:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// load an existing Visio diagram
String dataDir = Utils.getDataDir(ModifyVBAModuleCode.class);
InputStream input = new FileInputStream(dataDir + "macro.vsdm");
Diagram diagram = new Diagram(input);
// extract VBA project
VbaProject v = diagram.getVbaProject();
// Iterate through the modules and modify VBA macro code
for (int i = 0; i < diagram.getVbaProject().getModules().getCount(); i++) {
	VbaModule module = diagram.getVbaProject().getModules().get(i);
	String code = module.getCodes();
	if (code.contains("This is test message."))
		code = code.replace("This is test message.", "This is Aspose.Diagram message.");
	module.setCodes(code);
}
// save the Visio diagram
diagram.save(dataDir + "out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **Rimuovi tutte le macro da Visio Diagram**
Aspose.Diagram for Java consente agli sviluppatori di rimuovere tutte le macro da Visio diagram.

La proprietà JavaProjectData, esposta da[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, permette di rimuovere tutte le macro dal disegno Visio.
### **Esempio di programmazione Rimuovi tutte le macro**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RemoveMacrosFromVisio.class);  
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// remove all macros
diagram.setVbProjectData(null);

// Save diagram
diagram.save(dataDir + "RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
