---
title: Visio Zaman Çizgisi Şekillerini Yapılandırma
type: docs
weight: 50
url: /tr/net/configure-visio-timeline-shapes/
description: Bu bölümde, Aspose.Diagram ile kilometre taşı şeklinin özelliğinin nasıl ayarlanacağı açıklanmaktadır.
---
## **Kilometre Taşı Şekil Özelliklerini Ayarlama**
Aspose.Diagram, geliştiricilerin kilometre taşı özelliklerini belirlemesine olanak tanır. Bu makale kilometre taşı tarihi, tarih biçimi, otomatik güncelleme bayrağı ve türünün nasıl ayarlanacağını gösterir.
### **Kilometre Taşı Tarihini, Tarih Formatını, Otomatik Güncelleme Bayrağı ve Türünü Ayarlama**
 bu[Kilometre Taşı Yardımcısı](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)sınıf alır[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) başlatılırken nesne[Kilometre Taşı Yardımcısı](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) nesne. Bu makaledeki kod örneği, kilometre taşı tarihini, tarih biçimini, otomatik güncelleme bayrağını ve kilometre taşı türü özelliklerini ayarlar.

Kilometre taşı tarihini, tarih biçimini, otomatik güncelleme bayrağını ve kilometre taşı türünü güncelleme süreci:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. MilestoneHelper nesnesini başlatın.
1. Bir kilometre taşı tarihi belirleyin.
1. Kilometre taşı tarih biçimini ayarlayın.
1. Bir otomatik güncelleme bayrağı ayarlayın.
1. Kilometre taşı türünü ayarlayın
1. Visio çizimini desteklenen herhangi bir formatta kaydedin.
#### **Kilometre Taşı Programlama Örneği Ayarlama**

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



Tarih biçimi değerleri tablosu:

|**Değer**|**Dizeyi Biçimlendir**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|yyyy-AA-gg|
|2|yy-AAA-d|
|3|yyyy/A/d|
|4|yy-AAA.-d|
|5|d AAAA yyyy|
|6|y-M|
|7|MMM-yy|
|8|AAAa g, yyyy|
|9|AAA g, yyyy|
|10|Md-yy|
|11|MD|
|12|gAAA, yyyy|
|13|g AAA, yyyy|
|14|dM-yy|
|15|dM|
|16|yy-Md|
|17|yyyy-Md|
|18|M-yy|
|19|M-yyyy|
|20|AAAA yyyy|
|21|AAAA yy|
|22|AAA yyyy|
|23|AAA yy|
|24|yy|
|25|yyyy|
|26|d|
|27|AAAA|
|28|MMM|
|29|M|
## **Zaman Çizelgesi Şeklinin Zaman Dönemini ve Tarih Formatını Ayarlayın**
Aspose.Diagram, geliştiricilerin zaman çizelgesini programlı olarak yapılandırmasına olanak tanır. Bu, zaman çizelgesi şekillerinin (blok, çizgi, cetvel, bölünmüş veya silindirik) zaman periyodu ve tarih formatının nasıl ayarlanacağını açıklar.
### **Zaman Periyodu ve Tarih Formatının Ayarlanması**
 bu[Zaman Hattı Yardımcısı](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)sınıf alır[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) başlatırken nesne[Zaman Hattı Yardımcısı](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) nesne. Bu makaledeki kod örneği, dönem başlangıcı, bitişi ve tarih biçimi değerlerini ayarlar.

Zaman periyodu başlangıcı, bitişi ve tarih formatını güncelleme süreci şu şekildedir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. TimeLineHelper nesnesini başlatın.
1. Zaman aralığı başlangıcını ayarlayın.
1. Dönem sonunu ayarlayın.
1. Bir tarih formatı ayarlayın.
1. Visio çizimini desteklenen herhangi bir formatta kaydedin.
#### **Zaman Periyodu ve Tarih Programlama Örneği Ayarla**

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



Tarih biçimi değerleri tablosu:

|**Değer**|**Dizeyi Biçimlendir**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|yyyy-AA-gg|
|2|yy-AAA-d|
|3|yyyy/A/d|
|4|yy-AAA.-d|
|5|d AAAA yyyy|
|6|y-M|
|7|MMM-yy|
|8|AAAa g, yyyy|
|9|AAA g, yyyy|
|10|Md-yy|
|11|MD|
|12|gAAA, yyyy|
|13|g AAA, yyyy|
|14|dM-yy|
|15|dM|
|16|yy-Md|
|17|yyyy-Md|
|18|M-yy|
|19|M-yyyy|
|20|AAAA yyyy|
|21|AAAA yy|
|22|AAA yyyy|
|23|AAA yy|
|24|yy|
|25|yyyy|
|26|d|
|27|AAAA|
|28|MMM|
|29|M|
## **Visio'de Zaman Çizelgesinde Kilometre Taşlarını Yenile**
Aspose.Diagram, geliştiricilerin zaman aralığı değişikliğine göre zaman çizelgesi şekillerindeki (blok, çizgi, cetvel, bölünmüş veya silindirik) kilometre taşlarını ayarlamasına olanak tanır.
### **TimeLineHelper sınıfını kullanarak Zaman Çizelgesi'ndeki Kilometre Taşlarını yenileyin**
 Tarafından sunulan RefreshTimeLine yöntemi[Zaman Hattı Yardımcısı](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) class, zaman çizelgesindeki kilometre taşlarını canlandırmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. bir numune yükleyin diagram.
1. bir zaman çizelgesi şekli elde edin.
1. TimeLineHelper nesnesini başlatın.
1. zaman periyodunun başlangıcını ayarlayın.
1. zaman periyodunun sonunu ayarlayın.
1. tarih formatını ayarlayın (isteğe bağlı).
1. TimeLineHelper nesnesinin RefreshTimeLine yöntemini çağırın.
1. kaydet diagram
#### **TimeLineHelper Programlama Örneği Kullanarak Kilometre Taşlarını Yenileyin**
Aspose.Diagram for .NET'i kullanarak zaman çizelgesindeki kilometre taşlarını canlandırmak için .NET uygulamanızda aşağıdaki kodu kullanın.


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

### **MilestoneHelper sınıfını kullanarak Zaman Çizelgesi'ndeki Kilometre Taşlarını yenileyin**
 Tarafından sunulan RefreshMilestone yöntemi[Kilometre Taşı Yardımcısı](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)class, zaman çizelgesindeki kilometre taşlarını yenilemek için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. bir numune yükleyin diagram.
1. bir zaman çizelgesi şekli elde edin.
1. AddShape yöntemini kullanarak Visio diagram'de Shape ekleyin.
1. MilestoneHelper nesnesini başlatın.
1. Kilometre Taşı Tarihini ayarlayın.
1. Milstone'un IsAutoUpdate özelliğini true olarak ayarlayın.
1. MilestoneHelper nesnesinin RefreshMilestone yöntemini çağırın.
1. kaydet diagram
#### **MilestoneHelper Programlama Örneği Kullanarak Kilometre Taşlarını Yenileyin**
Aspose.Diagram for .NET'i kullanarak zaman çizelgesindeki kilometre taşlarını yenilemek için .NET uygulamanızda aşağıdaki kodu kullanın.


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

