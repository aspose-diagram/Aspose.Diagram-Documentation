---
title: Configure Visio TimeLine Shapes
type: docs
weight: 50
url: /net/configure-visio-timeline-shapes/
description: This section explains how to set the property of a milestone shape with Aspose.Diagram.
---

## **Set Milestone Shape Properties**
Aspose.Diagram allows developers to set milestone properties. This article shows how to set the milestone date, date format, auto update flag and type.
### **Setting Milestone Date, Date Format, Auto Update Flag and Type**
The [MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) class takes a [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object while initializing the [MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) object. The code example in this article sets the milestone date, date format, auto update flag and milestone type properties.

The process for updating the milestone date, date format, auto update flag and milestone type:

1. Load a diagram.
1. Find a particular shape.
1. Initialize the MilestoneHelper object.
1. Set a milestone date.
1. Set the milestone date format.
1. Set an auto update flag.
1. Set the milestone type
1. Save the Visio drawing to any supported format.
#### **Set Milestone Programming Sample**
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


Table of date format values:

|**Value**|**Format String**|
| :- | :- |
|0|dddd, yyyy-M-d|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|yyyy/M/d|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|M-d-yy|
|11|M-d|
|12|d MMMM, yyyy|
|13|d MMM, yyyy|
|14|d-M-yy|
|15|d-M|
|16|yy-M-d|
|17|yyyy-M-d|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|MMMM yy|
|22|MMM yyyy|
|23|MMM yy|
|24|yy|
|25|yyyy|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Set Time Period and Date Format of Timeline Shape**
Aspose.Diagram allows developers to configure the timeline programmatically. This explains how to adjust the time period and date format of timeline shapes (block, line, ruler, divided, or cylindrical).
### **Setting Time Period and Date Format**
The [TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) class takes a [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object when initializing the [TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) object. The code example in this article sets the time period start, end and date format values.

The process for updating time period start, end and date format is:

1. Load a diagram.
1. Find a particular shape.
1. Initialize the TimeLineHelper object.
1. Set the time period start.
1. Set the time period end.
1. Set a date format.
1. Save the Visio drawing to any supported format.
#### **Set Time Period and Date Programming Sample**
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


Table of date format values:

|**Value**|**Format String**|
| :- | :- |
|0|dddd, yyyy-M-d|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|yyyy/M/d|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|M-d-yy|
|11|M-d|
|12|d MMMM, yyyy|
|13|d MMM, yyyy|
|14|d-M-yy|
|15|d-M|
|16|yy-M-d|
|17|yyyy-M-d|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|MMMM yy|
|22|MMM yyyy|
|23|MMM yy|
|24|yy|
|25|yyyy|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Refresh Milestones on the Timeline in Visio**
Aspose.Diagram allows developers to adjust milestones on the timeline shapes (block, line, ruler, divided, or cylindrical) according to the time period change.
### **Refresh Milestones on the Timeline using TimeLineHelper class**
The RefreshTimeLine method exposed by the [TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) class can be used to revive milestones on the timeline.

The code below shows how to:

1. load a sample diagram.
1. get a timeline shape.
1. initialize the TimeLineHelper object.
1. set the time period start.
1. set the time period end.
1. set date format (optional).
1. call RefreshTimeLine method of the TimeLineHelper object.
1. save diagram
#### **Refresh Milestones using TimeLineHelper Programming Sample**
Use the following code in your .NET application to revive milestones on the timeline using Aspose.Diagram for .NET.

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
### **Refresh Milestones on the Timeline using MilestoneHelper class**
The RefreshMilestone method exposed by the [MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) class can be used to refresh milestones on the timeline.

The code below shows how to:

1. load a sample diagram.
1. get a timeline shape.
1. add Shape in Visio diagram using AddShape method.
1. initialize the MilestoneHelper object.
1. set Milestone Date.
1. set Milstone's IsAutoUpdate property to true.
1. call RefreshMilestone method of the MilestoneHelper object.
1. save diagram
#### **Refresh Milestones using MilestoneHelper Programming Sample**
Use the following code in your .NET application to refresh milestones on the timeline using Aspose.Diagram for .NET.

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
