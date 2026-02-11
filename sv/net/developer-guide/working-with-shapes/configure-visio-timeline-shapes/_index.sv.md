---
title: Konfigurera Visio Tidslinjeformer
type: docs
weight: 50
url: /sv/net/configure-visio-timeline-shapes/
description: Det här avsnittet förklarar hur du ställer in egenskapen för en milstolpeform med Aspose.Diagram.
---
## **Ställ in egenskaper för milstolpeform**
Aspose.Diagram tillåter utvecklare att ange milstolpsegenskaper. Den här artikeln visar hur du ställer in milstolpedatum, datumformat, flagga och typ för automatisk uppdatering.
### **Ställa in milstolpsdatum, datumformat, flagga för automatisk uppdatering och typ**
 De[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)klass tar en[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objekt medan du initierar[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) objekt. Kodexemplet i den här artikeln anger egenskaperna för milstolpedatum, datumformat, flagga för automatisk uppdatering och milstolpetyp.

Processen för uppdatering av milstolpsdatum, datumformat, flagga för automatisk uppdatering och milstolpetyp:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Initiera MilestoneHelper-objektet.
1. Sätt ett milstolpedatum.
1. Ställ in formatet för milstolpedatum.
1. Ställ in en flagga för automatisk uppdatering.
1. Ställ in milstolpetypen
1. Spara Visio-ritningen i valfritt format som stöds.
#### **Ställ in milstolpeprogrammeringsexempel**
```
{{< highlight "csharp" >}}
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
```


Tabell över datumformatvärden:

|**Värde**|**Formatera sträng**|
|:- |:- |
|0|dddd, åååå-Md|
|1|åååå-MM-dd|
|2|åå-MMM-d|
|3|åååå/m/d|
|4|åå-MMM.-d|
|5|d MMMM åååå|
|6|åå-M|
|7|MMM-åå|
|8|MMMM d, åååå|
|9|MMM d, åååå|
|10|Md-åå|
|11|Md|
|12|d MMMM, åååå|
|13|d MMM, åååå|
|14|dM-åå|
|15|dM|
|16|åå-Md|
|17|åååå-Md|
|18|M-åå|
|19|M-åååå|
|20|MMMM åååå|
|21|MMMM åå|
|22|MMM åååå|
|23|MMM åå|
|24|åå|
|25|åååå|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Ställ in tidsperiod och datumformat för tidslinjeform**
Aspose.Diagram tillåter utvecklare att konfigurera tidslinjen programmatiskt. Det här förklarar hur du justerar tidsperioden och datumformatet för tidslinjeformer (block, linje, linjal, delad eller cylindrisk).
### **Ställa in tidsperiod och datumformat**
 De[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)klass tar en[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objekt när du initierar[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) objekt. Kodexemplet i den här artikeln ställer in tidsperiodens start-, slut- och datumformatvärden.

Processen för att uppdatera tidsperiodens start-, slut- och datumformat är:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Initiera TimeLineHelper-objektet.
1. Ställ in tidsperiodens start.
1. Ställ in tidsperiodens slut.
1. Ställ in ett datumformat.
1. Spara Visio-ritningen i valfritt format som stöds.
#### **Ställ in tidsperiod och datumprogrammeringsexempel**
```
{{< highlight "csharp" >}}
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
```


Tabell över datumformatvärden:

|**Värde**|**Formatera sträng**|
|:- |:- |
|0|dddd, åååå-Md|
|1|åååå-MM-dd|
|2|åå-MMM-d|
|3|åååå/m/d|
|4|åå-MMM.-d|
|5|d MMMM åååå|
|6|åå-M|
|7|MMM-åå|
|8|MMMM d, åååå|
|9|MMM d, åååå|
|10|Md-åå|
|11|Md|
|12|d MMMM, åååå|
|13|d MMM, åååå|
|14|dM-åå|
|15|dM|
|16|åå-Md|
|17|åååå-Md|
|18|M-åå|
|19|M-åååå|
|20|MMMM åååå|
|21|MMMM åå|
|22|MMM åååå|
|23|MMM åå|
|24|åå|
|25|åååå|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Uppdatera milstolpar på tidslinjen i Visio**
Aspose.Diagram tillåter utvecklare att justera milstolpar på tidslinjeformerna (block, linje, linjal, delad eller cylindrisk) enligt tidsperiodens förändring.
### **Uppdatera milstolpar på tidslinjen med TimeLineHelper-klassen**
 Metoden RefreshTimeLine exponerad av[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) klass kan användas för att återuppliva milstolpar på tidslinjen.

Koden nedan visar hur man:

1. ladda ett prov diagram.
1. få en tidslinjeform.
1. initiera TimeLineHelper-objektet.
1. ställ in tidsperiodens start.
1. ställ in tidsperiodens slut.
1. ställ in datumformat (valfritt).
1. anropa RefreshTimeLine-metoden för TimeLineHelper-objektet.
1. spara diagram
#### **Uppdatera milstolpar med TimeLineHelper-programmeringsexempel**
Använd följande kod i din .NET-applikation för att återuppliva milstolpar på tidslinjen med Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
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
```
### **Uppdatera Milestones på tidslinjen med MilestoneHelper-klassen**
 RefreshMilestone-metoden exponerad av[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)klass kan användas för att uppdatera milstolpar på tidslinjen.

Koden nedan visar hur man:

1. ladda ett prov diagram.
1. få en tidslinjeform.
1. lägg till Shape i Visio diagram med AddShape-metoden.
1. initiera MilestoneHelper-objektet.
1. ställ in ett milstolpedatum.
1. ställ in Milstones IsAutoUpdate-egenskap till true.
1. anropa RefreshMilestone-metoden för MilestoneHelper-objektet.
1. spara diagram
#### **Uppdatera Milestones med hjälp av MilestoneHelper-programmeringsexempel**
Använd följande kod i din .NET-applikation för att uppdatera milstolpar på tidslinjen med Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
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
```
