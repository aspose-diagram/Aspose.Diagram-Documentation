---
title: Visio Shape'in XForm, Çizgi ve Dolgu Verilerini Ayarla
type: docs
weight: 70
url: /tr/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **XForm Verilerini Ayarlama**
 XForm öğesi, Microsoft Visio XML şemasının bir parçasıdır. XForm, örneğin genişlik, yükseklik, dönüş ve şeklin döndürülüp çevrilmediği gibi bir şekil konumu belirtir. bu[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) tarafından açığa çıkarılan mülk,[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) sınıfı, Aspose.Diagram.XForm nesnesini destekler. XForm özelliği, bir şeklin XForm verilerini almak veya güncellemek için kullanılabilir. Bu makaledeki kod örnekleri, sayfadaki şekilleri taşımak için PinX (X-koordinatı) ve PinY (Y-koordinatı) XForm değerlerini değiştirir.

**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram sonra** **PinX** **ve** **PinY** **değerler değiştirildi** 

![yapılacaklar:resim_alternatif_Metin](set-visio-shape-s-xform-line-and-fill-data_2.png)

XForm verilerini güncelleme işlemi şu şekildedir:

1. Bir diagram yükleyin.# Belirli bir şekil bulun.# Şeklin XForm verilerini güncelleyin.
1. diagram'i kaydedin.
### **Programlama Örneği**
Aşağıdaki kod parçacığı, bir şeklin XForm verilerinin nasıl güncelleneceğini gösterir. Kod, şekil kimliği 1 olan bir şekil adları sürecini arar ve X ve Y koordinatlarını 5 olarak ayarlar.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetXFormdata-SetXFormdata.java" >}}
## **Visio Şeklin Çizgi Verisini Ayarla**
Şekiller çeşitli şekillerde biçimlendirilebilir. Bu makale, bir satırın özniteliklerinin nasıl belirtileceğini gösterir.

Microsoft Visio, kullanıcıların satırları çeşitli şekillerde biçimlendirmesine olanak tanır. Aspose.Diagram for Java şunları destekler:

- Ağırlık: bir çizginin kalınlığı.
- Renk: şeklin çizgi rengini ayarlar.
- Çizgi Rengi Şeffaflığı: şeklin çizgi rengi şeffaflığını yüzde olarak ayarlayın.
- Desen: çizginin düz, kesikli veya başka bir desene sahip olup olmadığını tanımlar.
- Yuvarlama: köşelerin yarıçapı.
- Başlangıç ve bitiş okları: Satırda ok olup olmadığı belirtilir.
- Başlangıç ve bitiş ok boyutları: ok boyutlarını ayarlayın.
- Cap: Çizginin yuvarlanması biter.
### **Bir şeklin kenarlığının çizgi rengini, kalınlığını, tire tipini, saydamlığını, yuvarlamasını, ok tipini ve ok boyutunu değiştirin**
 bu[Astar](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) tarafından açığa çıkarılan mülk,[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)sınıfı, Aspose.Diagram.Line nesnesini destekler. Bu özellik, bir şeklin çizgi verilerini almak veya güncellemek için kullanılabilir.
#### **Hat Veri Programlama Örneği**
Aşağıdaki kod parçası, şeklin satır verilerini günceller.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetLineData-SetLineData.java" >}}
## **Visio Şeklin Dolgu Verisini Ayarla**
Şekiller çeşitli şekillerde biçimlendirilebilir. Bu konu, bir şeklin dolgusunun nasıl belirtileceğini açıklar.

 Microsoft Office Visio, kullanıcıların dolguları çeşitli şekillerde biçimlendirmesine olanak tanır. bu[Doldurmak](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) Aspose.Diagram for Java API sınıfı ayarı destekler:

- Arka plan ve ön plan renkleri.
- şeffaflık
- Kalıpları doldurun.
- gölgeler
### **Dolgu Değerlerini Ayarlama**
Shape sınıfı tarafından sunulan Fill özelliği, Aspose.Diagram.Fill nesnesini destekler. Fill özelliği, bir şeklin dolgu verilerini almak veya güncellemek için kullanılabilir.

|<p>**diagram girişi** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/OrhEecb.png)</p>|<p>**Dolgu rengini değiştirdikten sonra diagram** </p><p>![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Veri Programlama Örneği Doldur**
Aşağıdaki kod parçacığı, bir şeklin dolgu verilerini günceller. Kod, şekil kimliği 1 olan dikdörtgen adlı bir şekli arar ve dolgu arka planını ve ön plan renklerini ayarlar.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetFillData-SetFillData.java" >}}
### **Visio Şeklinin Miras Alınan Dolgu Verilerini Alma**
Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralma dolgu verilerini alabilir veya ayarlayabilir. Shape sınıfı tarafından sunulan InheritFill özelliği, üst stil ve ana şekil tarafından devralınan şekle ilişkin dolgu biçimlendirme değerlerini içerir.
#### **Devralınan Doldurma Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan dolgu verilerini alır. Lütfen bu örnek kodu kontrol edin:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveInheritedFillData-RetrieveInheritedFillData.java" >}}
