---
title: Configura Visio TimeLine Shapes
type: docs
weight: 50
url: /it/net/configure-visio-timeline-shapes/
description: Questa sezione spiega come impostare la proprietà di una forma cardine con Aspose.Diagram.
---
## **Imposta le proprietà della forma cardine**
Aspose.Diagram consente agli sviluppatori di impostare le proprietà cardine. Questo articolo mostra come impostare la data cardine, il formato della data, il flag e il tipo di aggiornamento automatico.
### **Impostazione della data del traguardo, del formato della data, del flag e del tipo di aggiornamento automatico**
 Il[Milestone Helper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)la classe prende a[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) oggetto durante l'inizializzazione del[Milestone Helper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) oggetto. L'esempio di codice in questo articolo imposta la data cardine, il formato della data, il flag di aggiornamento automatico e le proprietà del tipo cardine.

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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 22;
// Get timeline shape
Shape milestone = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Initialize MilestoneHelper object
Aspose.Diagram.MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

// Set milestone date
milestoneHelper.MilestoneDate = new DateTime(2014, 10, 21);
// Set date format
milestoneHelper.DateFormat = 21;
// Set auto update flag
milestoneHelper.IsAutoUpdate = true;
// Set milestone type
milestoneHelper.Type = 6;

// Save to VDX format
diagram.Save(dataDir + "SetMilestoneProps_out.vsdx", SaveFileFormat.VSDX);

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
 Il[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)la classe prende a[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) oggetto durante l'inizializzazione del[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) oggetto. L'esempio di codice in questo articolo imposta i valori del formato di inizio, fine e data del periodo di tempo.

Il processo per l'aggiornamento del formato di inizio, fine e data del periodo di tempo è:

1. Carica un diagram.
1. Trova una forma particolare.
1. Inizializzare l'oggetto TimeLineHelper.
1. Impostare l'inizio del periodo di tempo.
1. Impostare la fine del periodo di tempo.
1. Imposta un formato della data.
1. Salva il disegno Visio in qualsiasi formato supportato.
#### **Impostare il periodo di tempo e il campione di programmazione della data**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");
int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Initialize TimeLineHlper object
Aspose.Diagram.TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.TimePeriodStart = new DateTime(2014, 12, 21);
// Set end time
timelineHelper.TimePeriodFinish = new DateTime(2015, 2, 19);

// Set date format
// TimelineHelper.DateFormatForBE = 21;
// Set date format for intm of timeline shape   
// TimelineHelper.DateFormatForIntm = 21;

// Or

// Set date format string for start and finish of timeline shape
timelineHelper.DateFormatStringForBE = "yyyy-MM-dd";
// Set date format string for intm of timeline shape
timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd";

// Save to VDX format
diagram.Save(dataDir + "ConfigureTimeLine_out.vsdx", SaveFileFormat.VSDX);

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
 Il metodo RefreshTimeLine esposto da[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) la classe può essere utilizzata per far rivivere le pietre miliari sulla sequenza temporale.

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
Utilizza il seguente codice nella tua applicazione .NET per riattivare le pietre miliari sulla sequenza temporale utilizzando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

int shapeid = 1;
// Get timeline shape
Shape timeline = diagram.Pages.GetPage("Page-1").Shapes.GetShape(shapeid);

// Initialize TimeLineHlper object
TimeLineHelper timelineHelper = new TimeLineHelper(timeline);

// Set start time
timelineHelper.TimePeriodStart = new DateTime(2014, 12, 21);
// Set end time
timelineHelper.TimePeriodFinish = new DateTime(2015, 2, 19);

// Set date format
timelineHelper.DateFormatForBE = 21;

// Revive milestones on the timeline
timelineHelper.RefreshTimeLine();

// Save to VDX format
diagram.Save(dataDir + "RefreshTimeLine_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Aggiorna le pietre miliari sulla sequenza temporale utilizzando la classe MilestoneHelper**
 Il metodo RefreshMilestone esposto da[Milestone Helper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)la classe può essere utilizzata per aggiornare le pietre miliari sulla sequenza temporale.

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
Utilizzare il seguente codice nell'applicazione .NET per aggiornare le pietre miliari sulla sequenza temporale utilizzando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

string pageName = "Page-1";

////////////// Modify time line /////////// 
DateTime startDate = new DateTime(2015, 8, 1);
DateTime endDate = new DateTime(2016, 6, 1);
DateTime fisYear = startDate;

// Load a diagram 
Diagram diagram = new Diagram(dataDir + "DrawingTimeLine.vsdx");

// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(pageName);

long timelineId = 1;
Shape timeline = diagram.Pages.GetPage(pageName).Shapes.GetShape(timelineId);
double xpos = timeline.XForm.PinX.Value;
double ypos = timeline.XForm.PinY.Value;

// Add milestone 
string milestoneMasterName = "2 triangle milestone";

// Add Master
diagram.AddMaster(dataDir + "Timeline.vss", milestoneMasterName);

// Add Shape in Visio diagram using AddShape method
long milestoneShapeId = diagram.AddShape(xpos, ypos, milestoneMasterName, 0);

// Get the shape based on ID
Shape milestone = page.Shapes.GetShape(milestoneShapeId);

// Instantiate MilestoneHelper object
MilestoneHelper milestoneHelper = new MilestoneHelper(milestone);

// Set Milestone Date
milestoneHelper.MilestoneDate = new DateTime(2015, 8, 1);

// Set IsAutoUpdate to true
milestoneHelper.IsAutoUpdate = true;

// RefreshMilesone of timeline shape
milestoneHelper.RefreshMilestone(timeline);

// Save Visio file
diagram.Save(dataDir + "RefreshMilestone_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

