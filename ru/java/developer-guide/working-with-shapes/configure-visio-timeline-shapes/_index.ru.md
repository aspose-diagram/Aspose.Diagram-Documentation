---
title: Настроить Visio формы временной шкалы
type: docs
weight: 20
url: /ru/java/configure-visio-timeline-shapes/
---
## **Установить свойства формы вехи**
Aspose.Diagram позволяет разработчикам устанавливать свойства вех. В этой статье показано, как установить дату вехи, формат даты, флаг автоматического обновления и тип.
### **Установка даты вехи, формата даты, флага автоматического обновления и типа**
[Milestone Helper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)класс берет[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) объект при инициализации[Milestone Helper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper) объект. Пример кода в этой статье задает дату вехи, формат даты, флаг автоматического обновления и свойства типа вехи.

|<p>**Веха перед обновлением** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**Веха после обновления. Обратите внимание на измененный формат даты.** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
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
```
{{< highlight "java" >}}
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
```


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
[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)класс берет[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) объект при инициализации[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) объект. В примере кода в этой статье задаются значения формата начала, окончания и даты периода времени.

|<p>**Вкладка периода времени диалогового окна Visio Настройка временной шкалы** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/nHth3W8.png)</p>|<p>**Вкладка формата времени диалогового окна Visio Настройка временной шкалы** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](configure-visio-timeline-shapes_1.png)</p>|<p>**diagram после изменения значений** </p><p>![дело:изображение_альтернативный_текст](configure-visio-timeline-shapes_2.png)</p>|
Процесс обновления формата начала, окончания и даты периода времени:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Инициализируйте объект TimeLineHelper.
1. Установите начало периода времени.
1. Установите конец периода времени.
1. Установите формат даты.
1. Сохраните чертеж Visio в любом поддерживаемом формате.
#### **Пример программирования установки периода времени и даты**
```
{{< highlight "java" >}}
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
```


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
 Метод RefreshTimeLine, предоставляемый[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) можно использовать для восстановления вех на временной шкале.

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
Используйте следующий код в своем приложении Java, чтобы оживить вехи на временной шкале, используя Aspose.Diagram for Java.

```
{{< highlight "java" >}}
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
```
### **Обновление вех на временной шкале с помощью класса MilestoneHelper**
 Метод RefreshMilestone, предоставленный[Milestone Helper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)можно использовать для обновления вех на временной шкале.

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
Используйте следующий код в своем приложении Java, чтобы обновить вехи на временной шкале с помощью Aspose.Diagram for Java.

```
{{< highlight "java" >}}
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
```
