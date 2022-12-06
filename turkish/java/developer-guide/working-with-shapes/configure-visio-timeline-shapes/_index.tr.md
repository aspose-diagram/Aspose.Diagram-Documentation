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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-SetMilestoneProps-SetMilestoneProps.java" >}}


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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-ConfigureTimeLine-ConfigureTimeLine.java" >}}


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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshTimeLine-RefreshTimeLine.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshMilestoneWithMilestoneHelper-RefreshMilestoneWithMilestoneHelper.java" >}}
