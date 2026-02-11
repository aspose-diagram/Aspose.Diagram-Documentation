---
title: 配置 Visio 时间线形状
type: docs
weight: 50
url: /zh/net/configure-visio-timeline-shapes/
description: 本节介绍如何使用 Aspose.Diagram 设置里程碑形状的属性。
---
## **设置里程碑形状属性**
Aspose.Diagram 允许开发人员设置里程碑属性。本文介绍如何设置里程碑日期、日期格式、自动更新标志和类型。
### **设置里程碑日期、日期格式、自动更新标志和类型**
这[里程碑助手](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)上课需要一个[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)初始化时的对象[里程碑助手](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)目的。本文中的代码示例设置里程碑日期、日期格式、自动更新标志和里程碑类型属性。

更新里程碑日期、日期格式、自动更新标志和里程碑类型的过程：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 初始化 MilestoneHelper 对象。
1. 设置里程碑日期。
1. 设置里程碑日期格式。
1. 设置自动更新标志。
1. 设置里程碑类型
1. 将 Visio 图形保存为任何支持的格式。
#### **设置里程碑编程示例**
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


日期格式值表：

|**价值**|**格式化字符串**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|年/月/日|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|MD-YY|
|11|MD|
|12|d MMMM, yyyy|
|13|d 嗯，yyyy|
|14|dM-yy|
|15|分米|
|16|yy-Md|
|17|yyyy-MD|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|嗯嗯|
|22|嗯嗯嗯|
|23|嗯嗯|
|24|yy|
|25|yyyy|
|26|d|
|27|嗯嗯|
|28|嗯|
|29|米|
## **设置时间线形状的时间段和日期格式**
Aspose.Diagram 允许开发人员以编程方式配置时间线。这解释了如何调整时间线形状（块、线、标尺、分割或圆柱形）的时间段和日期格式。
### **设置时间段和日期格式**
这[时间线助手](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)上课需要一个[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)初始化时的对象[时间线助手](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)目的。本文中的代码示例设置时间段开始、结束和日期格式值。

更新时间段开始、结束和日期格式的过程是：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 初始化 TimeLineHelper 对象。
1. 设置时间段开始。
1. 设置时间段结束。
1. 设置日期格式。
1. 将 Visio 图形保存为任何支持的格式。
#### **设置时间段和日期编程示例**
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


日期格式值表：

|**价值**|**格式化字符串**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|年/月/日|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|MD-YY|
|11|MD|
|12|d MMMM, yyyy|
|13|d 嗯，yyyy|
|14|dM-yy|
|15|分米|
|16|yy-Md|
|17|yyyy-MD|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|嗯嗯|
|22|嗯嗯嗯|
|23|嗯嗯|
|24|yy|
|25|yyyy|
|26|d|
|27|嗯嗯|
|28|嗯|
|29|米|
## **刷新时间轴上的里程碑 Visio**
Aspose.Diagram 允许开发人员根据时间段变化调整时间轴形状（块、线、标尺、分割或圆柱形）上的里程碑。
### **使用 TimeLineHelper 类刷新时间轴上的里程碑**
公开的 RefreshTimeLine 方法[时间线助手](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)类可用于恢复时间轴上的里程碑。

下面的代码显示了如何：

1. 加载样本 diagram。
1. 得到一个时间线形状。
1. 初始化 TimeLineHelper 对象。
1. 设置时间段开始。
1. 设置时间段结束。
1. 设置日期格式（可选）。
1. 调用 TimeLineHelper 对象的 RefreshTimeLine 方法。
1. 保存 diagram
#### **使用 TimeLineHelper 编程示例刷新里程碑**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 恢复时间轴上的里程碑。

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
### **使用 MilestoneHelper 类刷新时间轴上的里程碑**
公开的 RefreshMilestone 方法[里程碑助手](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)类可用于刷新时间轴上的里程碑。

下面的代码显示了如何：

1. 加载样本 diagram。
1. 得到一个时间线形状。
1. 使用 AddShape 方法在 Visio diagram 添加 Shape。
1. 初始化 MilestoneHelper 对象。
1. 设置里程碑日期。
1. 将 Milstone 的 IsAutoUpdate 属性设置为 true。
1. 调用 MilestoneHelper 对象的 RefreshMilestone 方法。
1. 保存 diagram
#### **使用 MilestoneHelper 编程示例刷新里程碑**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 刷新时间轴上的里程碑。

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
