---
title: Configura Visio TimeLine Shapes
type: docs
weight: 20
url: /it/java/configure-visio-timeline-shapes/
---
## **Imposta le proprietà della forma cardine**
Aspose.Diagram consente agli sviluppatori di impostare le proprietà cardine. Questo articolo mostra come impostare la data cardine, il formato della data, il flag e il tipo di aggiornamento automatico.
### **Impostazione della data del traguardo, del formato della data, del flag e del tipo di aggiornamento automatico**
 Il[Milestone Helper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)la classe prende a[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) oggetto durante l'inizializzazione del[Milestone Helper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper) oggetto. L'esempio di codice in questo articolo imposta la data cardine, il formato della data, il flag di aggiornamento automatico e le proprietà del tipo cardine.

|<p>**La pietra miliare prima dell'aggiornamento** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**La pietra miliare dopo l'aggiornamento. Notare il formato della data modificato.** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
Il processo per l'aggiornamento della data del traguardo, del formato della data, del flag di aggiornamento automatico e del tipo di traguardo:

1. Carica un diagram.
1. Trova una forma particolare.
1. Inizializza l'oggetto MilestoneHelper.
1. Stabilisci una data importante.
1. Impostare il formato della data cardine.
1. Imposta un flag di aggiornamento automatico.
1. Imposta il tipo di traguardo
1. Salva il disegno Visio in qualsiasi formato supportato.
#### **Imposta campione di programmazione Milestone**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetMilestoneProps.class);  
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 22;
// Get timeline shape
Shape milestone = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

// Set milestone date
milestoneHelper.setMilestoneDate(new DateTime(2014, 10, 21));
// Set date format
milestoneHelper.setDateFormat(21);
// Set auto update flag
milestoneHelper.setAutoUpdate(true);
// Set milestone type
milestoneHelper.setType(6);

// Save to VDX format
diagram.save(dataDir + "SetMilestoneProps_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



Tabella dei valori del formato della data:

|**Valore**|**Formato stringa**|
|:- |:- |
|0|gggg, aaaa-Md|
|1|aaaa-MM-gg|
|2|aa-MMM-gg|
|3|aaaa/M/g|
|4|aa-MMM.-g|
|5|d MMMM aaaa|
|6|aa-M|
|7|MMM-aa|
|8|MMMM d, aaaa|
|9|MMM d, aaaa|
|10|Md-aa|
|11|Md|
|12|d MMMM, aaaa|
|13|d MMM, aaaa|
|14|dM-aa|
|15|dM|
|16|aa-mar|
|17|aaaa-Md|
|18|M-aa|
|19|M-aaaa|
|20|MMMM aaaa|
|21|MMMM aa|
|22|MMM aaaa|
|23|MMM aa|
|24|aa|
|25|aaaa|
|26|d|
|27|MMMM|
|28|Mmm|
|29|M|
## **Imposta il periodo di tempo e il formato della data della forma della sequenza temporale**
Aspose.Diagram consente agli sviluppatori di configurare la sequenza temporale in modo programmatico. Questo spiega come regolare il periodo di tempo e il formato della data delle forme della sequenza temporale (blocco, linea, righello, diviso o cilindrico).
### **Impostazione del periodo di tempo e del formato della data**
 Il[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)la classe prende a[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) oggetto durante l'inizializzazione del[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) oggetto. L'esempio di codice in questo articolo imposta i valori del formato di inizio, fine e data del periodo di tempo.

|<p>**La scheda del periodo di tempo della finestra di dialogo Configura sequenza temporale Visio** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/nHth3W8.png)</p>|<p>**La scheda del formato dell'ora della finestra di dialogo Configura sequenza temporale Visio** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**Inserisci diagram** </p><p>![cose da fare:immagine_alt_testo](configure-visio-timeline-shapes_1.png)</p>|<p>**Lo diagram dopo che i valori sono stati modificati** </p><p>![cose da fare:immagine_alt_testo](configure-visio-timeline-shapes_2.png)</p>|
Il processo per l'aggiornamento del formato di inizio, fine e data del periodo di tempo è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Inizializzare l'oggetto TimeLineHelper.
1. Impostare l'inizio del periodo di tempo.
1. Impostare la fine del periodo di tempo.
1. Imposta un formato della data.
1. Salva il disegno Visio in qualsiasi formato supportato.
#### **Impostare il periodo di tempo e il campione di programmazione della data**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConfigureTimeLine.class); 
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.setTimePeriodStart(new DateTime(2014, 12, 21));
// Set end time
timelineHelper.setTimePeriodFinish(new DateTime(2015, 2, 19));

// Set date format
//timelineHelper.setDateFormatForBE(21);
// Set date format for intm of timeline shape   
//timelineHelper.setDateFormatForIntm(21);

// Or

// Set date format string for start and finish of timeline shape
timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");
// Set date format string for intm of timeline shape
timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

// Save to VDX format
diagram.save(dataDir + "ConfigureTimeLine_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}



Tabella dei valori del formato della data:

|**Valore**|**Formato stringa**|
|:- |:- |
|0|gggg, aaaa-Md|
|1|aaaa-MM-gg|
|2|aa-MMM-gg|
|3|aaaa/M/g|
|4|aa-MMM.-g|
|5|d MMMM aaaa|
|6|aa-M|
|7|MMM-aa|
|8|MMMM d, aaaa|
|9|MMM d, aaaa|
|10|Md-aa|
|11|Md|
|12|d MMMM, aaaa|
|13|d MMM, aaaa|
|14|dM-aa|
|15|dM|
|16|aa-mar|
|17|aaaa-Md|
|18|M-aa|
|19|M-aaaa|
|20|MMMM aaaa|
|21|MMMM aa|
|22|MMM aaaa|
|23|MMM aa|
|24|aa|
|25|aaaa|
|26|d|
|27|MMMM|
|28|Mmm|
|29|M|
## **Aggiorna le pietre miliari sulla linea temporale in Visio**
Aspose.Diagram consente agli sviluppatori di regolare le pietre miliari sulle forme della sequenza temporale (blocco, linea, righello, diviso o cilindrico) in base alla modifica del periodo di tempo.
### **Aggiorna le pietre miliari sulla sequenza temporale utilizzando la classe TimeLineHelper**
 Il metodo RefreshTimeLine esposto da[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) la classe può essere utilizzata per far rivivere le pietre miliari sulla sequenza temporale.

Il codice seguente mostra come:

1. caricare un campione diagram.
1. ottenere una forma della sequenza temporale.
1. inizializzare l'oggetto TimeLineHelper.
1. impostare l'inizio del periodo di tempo.
1. impostare la fine del periodo di tempo.
1. impostare il formato della data (facoltativo).
1. chiama il metodo RefreshTimeLine dell'oggetto TimeLineHelper.
1. salvo diagram
#### **Aggiorna le pietre miliari utilizzando l'esempio di programmazione TimeLineHelper**
Utilizza il seguente codice nella tua applicazione Java per riattivare le pietre miliari sulla sequenza temporale utilizzando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RefreshTimeLine.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.getPages().getPage("Page-1").getShapes().getShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.setTimePeriodStart(new DateTime(2014, 12, 21));
// Set end time
timelineHelper.setTimePeriodFinish(new DateTime(2015, 2, 19));

// Set date format
timelineHelper.setDateFormatForBE(21);

//revive milestones on the timeline
timelineHelper.refreshTimeLine();

// Save to VDX format
diagram.save(dataDir + "RefreshTimeLine_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Aggiorna le pietre miliari sulla sequenza temporale utilizzando la classe MilestoneHelper**
 Il metodo RefreshMilestone esposto da[Milestone Helper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)la classe può essere utilizzata per aggiornare le pietre miliari sulla sequenza temporale.

Il codice seguente mostra come:

1. caricare un campione diagram.
1. ottenere una forma della sequenza temporale.
1. aggiungi Shape in Visio diagram utilizzando il metodo AddShape.
1. inizializzare l'oggetto MilestoneHelper.
1. impostare la data del traguardo.
1. impostare la proprietà IsAutoUpdate di Milstone su true.
1. chiama il metodo RefreshMilestone dell'oggetto MilestoneHelper.
1. salvo diagram
#### **Aggiorna le pietre miliari utilizzando l'esempio di programmazione MilestoneHelper**
Utilizzare il seguente codice nell'applicazione Java per aggiornare le pietre miliari sulla sequenza temporale utilizzando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RefreshMilestoneWithMilestoneHelper.class);
        
String pageName = "Page-1";

////////////// Modify time line /////////// 
DateTime startDate = new DateTime(2015, 8, 1);
DateTime endDate = new DateTime(2016, 6, 1);
DateTime fisYear = startDate;

//Load a diagram 
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

//Get page
Page page = diagram.getPages().getPage(pageName);

long timelineId = 1;
Shape timeline = diagram.getPages().getPage(pageName).getShapes().getShape(timelineId);
double xpos = timeline.getXForm().getPinX().getValue();
double ypos = timeline.getXForm().getPinY().getValue();

// Add milestone 
String milestoneMasterName = "2 triangle milestone";

//Add Master
diagram.addMaster(dataDir + "Timeline.vss", milestoneMasterName);

//Add Shape in Visio diagram using AddShape method
long milestoneShapeId = diagram.addShape(xpos, ypos, milestoneMasterName, 0);

//Get the shape based on ID
Shape milestone = page.getShapes().getShape(milestoneShapeId);

//Instantiate MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

//Set Milestone Date
milestoneHelper.setMilestoneDate(new DateTime(2015, 8, 1));

//Set IsAutoUpdate to true
milestoneHelper.setAutoUpdate(true);

//RefreshMilesone of timeline shape
milestoneHelper.refreshMilestone(timeline);

//Save Visio file
diagram.save(dataDir + "RefreshMilestone_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

