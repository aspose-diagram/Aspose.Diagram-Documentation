---
title: Настроить Visio формы временной шкалы
type: docs
weight: 50
url: /ru/net/configure-visio-timeline-shapes/
description: В этом разделе объясняется, как установить свойство формы вехи с помощью Aspose.Diagram.
---
## **Установить свойства формы вехи**
Aspose.Diagram позволяет разработчикам устанавливать свойства вех. В этой статье показано, как установить дату вехи, формат даты, флаг автоматического обновления и тип.
### **Установка даты вехи, формата даты, флага автоматического обновления и типа**
[Milestone Helper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)класс берет[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) объект при инициализации[Milestone Helper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) объект. Пример кода в этой статье задает дату вехи, формат даты, флаг автоматического обновления и свойства типа вехи.

Процесс обновления даты вехи, формата даты, флага автоматического обновления и типа вехи:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Инициализируйте объект MilestoneHelper.
1. Установите контрольную дату.
1. Установите формат даты вехи.
1. Установите флаг автообновления.
1. Установите тип вехи
1. Сохраните чертеж Visio в любом поддерживаемом формате.
#### **Установить образец программирования Milestone**

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



Таблица значений формата даты:

|**Ценность**|**Строка формата**|
|:- |:- |
|0|дддд, гггг-Мд|
|1|гггг-мм-дд|
|2|гг-МММ-д|
|3|гггг/м/д|
|4|гг-МММ.-д|
|5|д ММММ гггг|
|6|гг-м|
|7|МММ-гг|
|8|ММММ д, гггг|
|9|МММ д, гггг|
|10|Мд-гг|
|11|Мэриленд|
|12|д ММММ, гггг|
|13|д МММ, гггг|
|14|дМ-гг|
|15|дм|
|16|гг-Мд|
|17|гггг-Мд|
|18|М-гг|
|19|М-гггг|
|20|ММММ гггг|
|21|ММММ гг|
|22|МММ гггг|
|23|МММ гг|
|24|гг|
|25|гггг|
|26|г|
|27|ММММ|
|28|М-М-М|
|29|М|
## **Установите период времени и формат даты формы временной шкалы**
Aspose.Diagram позволяет разработчикам настраивать временную шкалу программно. Здесь объясняется, как настроить период времени и формат даты для форм временной шкалы (блок, линия, линейка, разделенная или цилиндрическая).
### **Установка периода времени и формата даты**
[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)класс берет[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) объект при инициализации[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) объект. В примере кода в этой статье задаются значения формата начала, окончания и даты периода времени.

Процесс обновления формата начала, окончания и даты периода времени:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Инициализируйте объект TimeLineHelper.
1. Установите начало периода времени.
1. Установите конец периода времени.
1. Установите формат даты.
1. Сохраните чертеж Visio в любом поддерживаемом формате.
#### **Пример программирования установки периода времени и даты**

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



Таблица значений формата даты:

|**Ценность**|**Строка формата**|
|:- |:- |
|0|дддд, гггг-Мд|
|1|гггг-мм-дд|
|2|гг-МММ-д|
|3|гггг/м/д|
|4|гг-МММ.-д|
|5|д ММММ гггг|
|6|гг-м|
|7|МММ-гг|
|8|ММММ д, гггг|
|9|МММ д, гггг|
|10|Мд-гг|
|11|Мэриленд|
|12|д ММММ, гггг|
|13|д МММ, гггг|
|14|дМ-гг|
|15|дм|
|16|гг-Мд|
|17|гггг-Мд|
|18|М-гг|
|19|М-гггг|
|20|ММММ гггг|
|21|ММММ гг|
|22|МММ гггг|
|23|МММ гг|
|24|гг|
|25|гггг|
|26|г|
|27|ММММ|
|28|М-М-М|
|29|М|
## **Обновить вехи на временной шкале в Visio**
Aspose.Diagram позволяет разработчикам настраивать вехи на формах временной шкалы (блок, линия, линейка, разделенная или цилиндрическая) в соответствии с изменением периода времени.
### **Обновление вех на временной шкале с помощью класса TimeLineHelper**
 Метод RefreshTimeLine, предоставляемый[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) можно использовать для восстановления вех на временной шкале.

В приведенном ниже коде показано, как:

1. загрузить образец diagram.
1. получить форму временной шкалы.
1. инициализировать объект TimeLineHelper.
1. установить начало периода времени.
1. установить конец периода времени.
1. установить формат даты (необязательно).
1. вызвать метод RefreshTimeLine объекта TimeLineHelper.
1. сохранить diagram
#### **Обновление вех с помощью примера программирования TimeLineHelper**
Используйте следующий код в своем приложении .NET, чтобы оживить вехи на временной шкале, используя Aspose.Diagram for .NET.


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

### **Обновление вех на временной шкале с помощью класса MilestoneHelper**
 Метод RefreshMilestone, предоставленный[Milestone Helper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)можно использовать для обновления вех на временной шкале.

В приведенном ниже коде показано, как:

1. загрузить образец diagram.
1. получить форму временной шкалы.
1. добавьте Shape в Visio diagram, используя метод AddShape.
1. инициализировать объект MilestoneHelper.
1. установить контрольную дату.
1. установите для свойства Milstone IsAutoUpdate значение true.
1. вызвать метод RefreshMilestone объекта MilestoneHelper.
1. сохранить diagram
#### **Обновление вех с помощью примера программирования MilestoneHelper**
Используйте следующий код в своем приложении .NET, чтобы обновить вехи на временной шкале с помощью Aspose.Diagram for .NET.


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

