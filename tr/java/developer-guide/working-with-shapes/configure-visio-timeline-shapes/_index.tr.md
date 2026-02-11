---
title: Visio Zaman Çizgisi Şekillerini Yapılandırma
type: docs
weight: 20
url: /tr/java/configure-visio-timeline-shapes/
---
## **Kilometre Taşı Şekil Özelliklerini Ayarlama**
Aspose.Diagram, geliştiricilerin kilometre taşı özelliklerini belirlemesine olanak tanır. Bu makale kilometre taşı tarihi, tarih biçimi, otomatik güncelleme bayrağı ve türünün nasıl ayarlanacağını gösterir.
### **Kilometre Taşı Tarihini, Tarih Formatını, Otomatik Güncelleme Bayrağı ve Türünü Ayarlama**
 bu[Kilometre Taşı Yardımcısı](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)sınıf alır[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) başlatılırken nesne[Kilometre Taşı Yardımcısı](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper) nesne. Bu makaledeki kod örneği, kilometre taşı tarihini, tarih biçimini, otomatik güncelleme bayrağını ve kilometre taşı türü özelliklerini ayarlar.

|<p>**Güncellemeden önceki dönüm noktası** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**Güncellemeden sonraki dönüm noktası. Değiştirilen tarih formatına dikkat edin.** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
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
 bu[Zaman Hattı Yardımcısı](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)sınıf alır[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) başlatırken nesne[Zaman Hattı Yardımcısı](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) nesne. Bu makaledeki kod örneği, dönem başlangıcı, bitişi ve tarih biçimi değerlerini ayarlar.

|<p>**Visio Zaman Çizelgesini Yapılandır iletişim kutusunun zaman aralığı sekmesi** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/nHth3W8.png)</p>|<p>**Visio Zaman Çizelgesini Yapılandır iletişim kutusunun saat formatı sekmesi** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**Giriş diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](configure-visio-timeline-shapes_1.png)</p>|<p>**Değerler değiştirildikten sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](configure-visio-timeline-shapes_2.png)</p>|
Zaman periyodu başlangıcı, bitişi ve tarih formatını güncelleme süreci şu şekildedir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. TimeLineHelper nesnesini başlatın.
1. Zaman aralığı başlangıcını ayarlayın.
1. Dönem sonunu ayarlayın.
1. Bir tarih formatı ayarlayın.
1. Visio çizimini desteklenen herhangi bir formatta kaydedin.
#### **Zaman Periyodu ve Tarih Programlama Örneği Ayarla**
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
 Tarafından sunulan RefreshTimeLine yöntemi[Zaman Hattı Yardımcısı](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) class, zaman çizelgesindeki kilometre taşlarını canlandırmak için kullanılabilir.

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
Aspose.Diagram for Java'i kullanarak zaman çizelgesindeki kilometre taşlarını canlandırmak için Java uygulamanızda aşağıdaki kodu kullanın.

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
### **MilestoneHelper sınıfını kullanarak Zaman Çizelgesi'ndeki Kilometre Taşlarını yenileyin**
 Tarafından sunulan RefreshMilestone yöntemi[Kilometre Taşı Yardımcısı](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)class, zaman çizelgesindeki kilometre taşlarını yenilemek için kullanılabilir.

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
Aspose.Diagram for Java'i kullanarak zaman çizelgesindeki kilometre taşlarını yenilemek için Java uygulamanızda aşağıdaki kodu kullanın.

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
