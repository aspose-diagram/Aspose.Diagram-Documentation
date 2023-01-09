---
title: Visio Shape'in XForm, Çizgi ve Dolgu Verilerini Ayarla
type: docs
weight: 20
url: /tr/net/set-visio-shape-s-xform-line-and-fill-data/
description: Bu bölümde, çizgi verileri dahil şeklin stilinin nasıl ayarlanacağı ve Aspose.Diagram ile verilerin nasıl doldurulacağı açıklanmaktadır.
---
## **XForm Verilerini Ayarlama**
 XForm öğesi, Microsoft Visio XML şemasının bir parçasıdır. XForm, örneğin genişlik, yükseklik, dönüş ve şeklin döndürülüp çevrilmediği gibi bir şekil konumu belirtir. bu[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) tarafından açığa çıkarılan mülk,[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıfı, Aspose.Diagram.XForm nesnesini destekler. XForm özelliği, bir şeklin XForm verilerini almak veya güncellemek için kullanılabilir. Bu makaledeki kod örnekleri, sayfadaki şekilleri taşımak için PinX (X-koordinatı) ve PinY (Y-koordinatı) XForm değerlerini değiştirir.

XForm verilerini güncelleme işlemi şu şekildedir:

1. Bir diagram yükleyin.# Belirli bir şekil bulun.# Şeklin XForm verilerini güncelleyin.
1. diagram'i kaydedin.
### **Programlama Örneği**
Aşağıdaki kod parçacığı, bir şeklin XForm verilerinin nasıl güncelleneceğini gösterir. Kod, şekil kimliği 1 olan bir şekil adları sürecini arar ve X ve Y koordinatlarını 5 olarak ayarlar.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **Visio Şeklin Çizgi Verisini Ayarla**
Şekiller çeşitli şekillerde biçimlendirilebilir. Bu makale, bir satırın özniteliklerinin nasıl belirtileceğini gösterir.

Microsoft Visio, kullanıcıların satırları çeşitli şekillerde biçimlendirmesine olanak tanır. Aspose.Diagram for .NET şunları destekler:

- Ağırlık: bir çizginin kalınlığı.
- Renk: şeklin çizgi rengini ayarlar.
- Çizgi Rengi Şeffaflığı: şeklin çizgi rengi şeffaflığını yüzde olarak ayarlayın.
- Desen: çizginin düz, kesikli veya başka bir desene sahip olup olmadığını tanımlar.
- Yuvarlama: köşelerin yarıçapı.
- Başlangıç ve bitiş okları: Satırda ok olup olmadığı belirtilir.
- Başlangıç ve bitiş ok boyutları: ok boyutlarını ayarlayın.
- Cap: Çizginin yuvarlanması biter.
### **Bir şeklin kenarlığının çizgi rengini, kalınlığını, tire tipini, saydamlığını, yuvarlamasını, ok tipini ve ok boyutunu değiştirin**
 bu[Astar](http://www.aspose.com/api/net/diagram/aspose.diagram/line) tarafından açığa çıkarılan mülk,[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)sınıfı, Aspose.Diagram.Line nesnesini destekler. Bu özellik, bir şeklin çizgi verilerini almak veya güncellemek için kullanılabilir.
#### **Hat Veri Programlama Örneği**
Aşağıdaki kod parçası, şeklin satır verilerini günceller.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **Visio Şeklin Dolgu Verisini Ayarla**
 Şekiller çeşitli şekillerde biçimlendirilebilir. Bu konu, bir şeklin dolgusunun nasıl belirtileceğini açıklar. Microsoft Office Visio, kullanıcıların dolguları çeşitli şekillerde biçimlendirmesine olanak tanır. bu[Doldurmak](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) Aspose.Diagram for .NET API sınıfı ayarı destekler:

- Arka plan ve ön plan renkleri.
- şeffaflık
- Kalıpları doldurun.
- gölgeler
### **Dolgu Değerlerini Ayarlama**
 Tarafından sunulan Fill özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf, destekler[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) nesne. Fill özelliği, bir şeklin dolgu verilerini almak veya güncellemek için kullanılabilir.
#### **Veri Programlama Örneği Doldur**
Aşağıdaki kod parçacığı, bir şeklin dolgu verilerini günceller. Kod, şekil kimliği 1 olan dikdörtgen adlı bir şekli arar ve dolgu arka planını ve ön plan renklerini ayarlar.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **Visio Şeklinin Miras Alınan Dolgu Verilerini Alma**
 Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin devralma dolgu verilerini alabilir veya ayarlayabilir. Tarafından sunulan InheritFill özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, ana stil ve ana şekil tarafından devralınan şeklin dolgu biçimlendirme değerlerini içerir.
#### **Devralınan Doldurma Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan dolgu verilerini alır. Lütfen bu örnek kodu kontrol edin:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
