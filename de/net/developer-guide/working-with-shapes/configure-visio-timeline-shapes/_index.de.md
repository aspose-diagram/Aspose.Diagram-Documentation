---
title: Konfigurieren Sie Visio TimeLine-Shapes
type: docs
weight: 50
url: /de/net/configure-visio-timeline-shapes/
description: In diesem Abschnitt wird erläutert, wie Sie die Eigenschaft einer Meilensteinform mit Aspose.Diagram festlegen.
---
## **Legen Sie die Eigenschaften der Meilensteinform fest**
Aspose.Diagram ermöglicht es Entwicklern, Meilensteineigenschaften festzulegen. Dieser Artikel zeigt, wie Sie das Datum des Meilensteins, das Datumsformat, das Flag und den Typ für die automatische Aktualisierung festlegen.
### **Festlegen von Meilensteindatum, Datumsformat, Auto-Update-Flag und Typ**
 Das[MeilensteinHelfer](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)Klasse dauert ein[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Objekt beim Initialisieren der[MeilensteinHelfer](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) Objekt. Das Codebeispiel in diesem Artikel legt die Eigenschaften Meilensteindatum, Datumsformat, Kennzeichen für automatische Aktualisierung und Meilensteintyp fest.

Der Vorgang zum Aktualisieren des Meilensteindatums, des Datumsformats, der Markierung für die automatische Aktualisierung und des Meilensteintyps:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Initialisieren Sie das MilestoneHelper-Objekt.
1. Legen Sie ein Meilensteindatum fest.
1. Legen Sie das Meilenstein-Datumsformat fest.
1. Setzen Sie ein Auto-Update-Flag.
1. Legen Sie den Meilensteintyp fest
1. Speichern Sie die Zeichnung Visio in einem beliebigen unterstützten Format.
#### **Programmierbeispiel für Meilenstein setzen**

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



Tabelle der Datumsformatwerte:

|**Wert**|**Zeichenkette formatieren**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|JJJJ-MM-TT|
|2|jj-MMM-d|
|3|JJJJ/M/T|
|4|jj-MMM.-d|
|5|d MMMM jjjj|
|6|jj-M|
|7|MMM-yy|
|8|MMMM d, jjjj|
|9|MMM d, jjjj|
|10|Md-jj|
|11|Md|
|12|d MMMM, jjjj|
|13|d MMM, jjjj|
|14|dM-jj|
|15|dm|
|16|jj-Md|
|17|jjjj-Md|
|18|M-jj|
|19|M-jjjj|
|20|MMMM yyyy|
|21|MMMM ja|
|22|MMM yyyy|
|23|MMM ja|
|24|jj|
|25|jjjj|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Legen Sie den Zeitraum und das Datumsformat der Zeitachsenform fest**
Aspose.Diagram ermöglicht es Entwicklern, die Zeitleiste programmgesteuert zu konfigurieren. Hier wird erklärt, wie Sie den Zeitraum und das Datumsformat von Zeitachsenformen (Block, Linie, Lineal, geteilt oder zylindrisch) anpassen.
### **Zeitraum und Datumsformat einstellen**
 Das[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)Klasse dauert ein[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Objekt beim Initialisieren der[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) Objekt. Das Codebeispiel in diesem Artikel legt die Start-, End- und Datumsformatwerte für den Zeitraum fest.

Der Prozess zum Aktualisieren des Start-, End- und Datumsformats des Zeitraums ist:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Initialisieren Sie das TimeLineHelper-Objekt.
1. Legen Sie den Beginn des Zeitraums fest.
1. Stellen Sie das Ende des Zeitraums ein.
1. Legen Sie ein Datumsformat fest.
1. Speichern Sie die Zeichnung Visio in einem beliebigen unterstützten Format.
#### **Programmierungsbeispiel für Zeitraum und Datum einstellen**

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



Tabelle der Datumsformatwerte:

|**Wert**|**Zeichenkette formatieren**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|JJJJ-MM-TT|
|2|jj-MMM-d|
|3|JJJJ/M/T|
|4|jj-MMM.-d|
|5|d MMMM jjjj|
|6|jj-M|
|7|MMM-yy|
|8|MMMM d, jjjj|
|9|MMM d, jjjj|
|10|Md-jj|
|11|Md|
|12|d MMMM, jjjj|
|13|d MMM, jjjj|
|14|dM-jj|
|15|dm|
|16|jj-Md|
|17|jjjj-Md|
|18|M-jj|
|19|M-jjjj|
|20|MMMM yyyy|
|21|MMMM ja|
|22|MMM yyyy|
|23|MMM ja|
|24|jj|
|25|jjjj|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Aktualisieren Sie Meilensteine auf der Zeitachse in Visio**
Aspose.Diagram ermöglicht es Entwicklern, Meilensteine auf den Zeitachsenformen (Block, Linie, Lineal, geteilt oder zylindrisch) entsprechend der Änderung des Zeitraums anzupassen.
### **Aktualisieren Sie Meilensteine auf der Timeline mithilfe der TimeLineHelper-Klasse**
 Die RefreshTimeLine-Methode, die von der bereitgestellt wird[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) Klasse kann verwendet werden, um Meilensteine auf der Zeitachse wiederzubeleben.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. Holen Sie sich eine Zeitleistenform.
1. Initialisieren Sie das TimeLineHelper-Objekt.
1. Legen Sie den Beginn des Zeitraums fest.
1. stellen Sie das Ende des Zeitraums ein.
1. Datumsformat festlegen (optional).
1. Rufen Sie die RefreshTimeLine-Methode des TimeLineHelper-Objekts auf.
1. außer diagram
#### **Aktualisieren Sie Meilensteine mit dem TimeLineHelper-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um Meilensteine auf der Zeitachse mit Aspose.Diagram for .NET wiederzubeleben.


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

### **Aktualisieren Sie Meilensteine auf der Timeline mithilfe der MilestoneHelper-Klasse**
 Die RefreshMilestone-Methode, die von der bereitgestellt wird[MeilensteinHelfer](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)-Klasse kann verwendet werden, um Meilensteine auf der Zeitachse zu aktualisieren.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. Holen Sie sich eine Zeitleistenform.
1. Fügen Sie Shape in Visio diagram mit der AddShape-Methode hinzu.
1. Initialisieren Sie das MilestoneHelper-Objekt.
1. Meilensteindatum festlegen.
1. Setzen Sie die IsAutoUpdate-Eigenschaft von Milstone auf true.
1. Rufen Sie die RefreshMilestone-Methode des MilestoneHelper-Objekts auf.
1. außer diagram
#### **Aktualisieren Sie Meilensteine mit dem MilestoneHelper-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um Meilensteine auf der Zeitachse mit Aspose.Diagram for .NET zu aktualisieren.


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

