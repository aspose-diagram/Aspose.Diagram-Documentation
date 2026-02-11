---
title: تكوين Visio أشكال الخط الزمني
type: docs
weight: 50
url: /ar/net/configure-visio-timeline-shapes/
description: يوضح هذا القسم كيفية تعيين خاصية شكل حدث رئيسي باستخدام Aspose.Diagram.
---
## **تعيين خصائص شكل الحدث**
Aspose.Diagram يسمح للمطورين بتعيين الخصائص الرئيسية. توضح هذه المقالة كيفية تعيين تاريخ الحدث وتنسيق التاريخ وعلامة التحديث التلقائي والنوع.
### **تحديد تاريخ الحدث وتنسيق التاريخ وعلامة التحديث التلقائي والنوع**
 ال[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)فئة تأخذ أ[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) الكائن أثناء تهيئة[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) هدف. يعيّن مثال الرمز في هذه المقالة تاريخ الحدث الرئيسي وتنسيق التاريخ وعلامة التحديث التلقائي وخصائص نوع الحدث الرئيسي.

عملية تحديث تاريخ الحدث وتنسيق التاريخ وعلامة التحديث التلقائي ونوع الحدث الرئيسي:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. تهيئة كائن MilestoneHelper.
1. حدد تاريخًا هامًا.
1. قم بتعيين تنسيق تاريخ الحدث.
1. تعيين علم التحديث التلقائي.
1. قم بتعيين نوع الحدث الرئيسي
1. احفظ Visio الرسم بأي تنسيق مدعوم.
#### **تعيين عينة البرمجة الرئيسية**

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



جدول قيم تنسيق التاريخ:

|**قيمة**|**تنسيق السلسلة**|
|:- |:- |
|0|dddd ، yyyy-Md|
|1|yyyy-MM-dd|
|2|س ص- ش ش ش- د|
|3|س س س / ش / د|
|4|س ص- ش ش ش- د|
|5|d MMMM yyyy|
|6|س ص- م|
|7|MMM-yy|
|8|d MMMM ، yyyy|
|9|d MMM ، yyyy|
|10|Md-yy|
|11|ام دي|
|12|d MMMM ، yyyy|
|13|d MMM ، yyyy|
|14|dM-yy|
|15|د م|
|16|س ص- Md|
|17|yyyy-Md|
|18|م ص|
|19|M-yyyy|
|20|MMMM yyyy|
|21|MMMM yy|
|22|MMM yyyy|
|23|MMM yy|
|24|س ص|
|25|س س س س|
|26|د|
|27|ش ش ش ش|
|28|MMM|
|29|م|
## **تعيين الفترة الزمنية وتنسيق التاريخ لشكل المخطط الزمني**
Aspose.Diagram يسمح للمطورين بتوصيف الجدول الزمني برمجيًا. يوضح هذا كيفية ضبط الفترة الزمنية وتنسيق التاريخ لأشكال المخطط الزمني (كتلة أو خط أو مسطرة أو مقسمة أو أسطوانية).
### **تحديد الفترة الزمنية وتنسيق التاريخ**
 ال[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)فئة تأخذ أ[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) الكائن عند تهيئة[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) هدف. يعيّن مثال الرمز في هذه المقالة قيم تنسيق بداية الفترة الزمنية والانتهاء والتاريخ.

عملية تحديث تنسيق بداية الفترة الزمنية وانتهائها وتاريخها هي:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. تهيئة كائن TimeLineHelper.
1. اضبط بداية الفترة الزمنية.
1. قم بتعيين نهاية الفترة الزمنية.
1. قم بتعيين تنسيق التاريخ.
1. احفظ Visio الرسم بأي تنسيق مدعوم.
#### **تعيين الفترة الزمنية وعينة تاريخ البرمجة**

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



جدول قيم تنسيق التاريخ:

|**قيمة**|**تنسيق السلسلة**|
|:- |:- |
|0|dddd ، yyyy-Md|
|1|yyyy-MM-dd|
|2|س ص- ش ش ش- د|
|3|س س س / ش / د|
|4|س ص- ش ش ش- د|
|5|d MMMM yyyy|
|6|س ص- م|
|7|MMM-yy|
|8|d MMMM ، yyyy|
|9|d MMM ، yyyy|
|10|Md-yy|
|11|ام دي|
|12|d MMMM ، yyyy|
|13|d MMM ، yyyy|
|14|dM-yy|
|15|د م|
|16|س ص- Md|
|17|yyyy-Md|
|18|م ص|
|19|M-yyyy|
|20|MMMM yyyy|
|21|MMMM yy|
|22|MMM yyyy|
|23|MMM yy|
|24|س ص|
|25|س س س س|
|26|د|
|27|ش ش ش ش|
|28|MMM|
|29|م|
## **تحديث المعالم على الجدول الزمني في Visio**
Aspose.Diagram يسمح للمطورين بضبط المعالم على أشكال الخط الزمني (كتلة أو خط أو مسطرة أو مقسمة أو أسطوانية) وفقًا لتغير الفترة الزمنية.
### **قم بتحديث الأحداث الرئيسية على المخطط الزمني باستخدام فئة TimeLineHelper**
 طريقة RefreshTimeLine التي تعرضها ملف[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) يمكن استخدام فئة لإحياء المعالم على الخط الزمني.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على شكل الجدول الزمني.
1. تهيئة كائن TimeLineHelper.
1. ضبط بداية الفترة الزمنية.
1. تعيين نهاية الفترة الزمنية.
1. ضبط تنسيق التاريخ (اختياري).
1. استدعاء أسلوب RefreshTimeLine للكائن TimeLineHelper.
1. احفظ diagram
#### **تحديث المعالم باستخدام نموذج برمجة TimeLineHelper**
استخدم الكود التالي في تطبيق .NET الخاص بك لإحياء المعالم على الخط الزمني باستخدام Aspose.Diagram for .NET.


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

### **تحديث المعالم على الخط الزمني باستخدام فئة MilestoneHelper**
 طريقة RefreshMilestone التي كشف عنها[MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)يمكن استخدام فئة لتحديث المعالم على الخط الزمني.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على شكل الجدول الزمني.
1. أضف الشكل Visio diagram باستخدام طريقة AddShape.
1. تهيئة كائن MilestoneHelper.
1. تعيين التاريخ الرئيسي.
1. تعيين خاصية Milstone's IsAutoUpdate إلى true.
1. استدعاء طريقة RefreshMilestone للكائن MilestoneHelper.
1. احفظ diagram
#### **تحديث المعالم باستخدام نموذج برمجة MilestoneHelper**
استخدم الكود التالي في تطبيق .NET لتحديث المعالم على الخط الزمني باستخدام Aspose.Diagram for .NET.


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

