---
title: Aspose.Diagram Nesne Modeli
linktitle: Aspose.Diagram Nesne Modeli
type: docs
description: Aspose.Diagram Nesne Modeli, Aspose.Diagram sınıf kitaplığının nesneleri arasındaki yapısal ilişkiler hakkında bilgi sağlar.
weight: 20
url: /tr/net/object_model
---
{{% alert color="primary" %}} 

**Aspose.Diagram Nesne Modeli**

Aspose.Diagram Nesne Modeli, Aspose.Diagram sınıf kitaplığının nesneleri arasındaki yapısal ilişkiler hakkında bilgi sağlar.

{{% /alert %}} 

### Aspose.Diagram nesne modelinin üst düzey yapısı aşağıda hiyerarşik olarak gösterilmiştir.

|**Aspose.Diagram Nesne Modeli'nin üst düzey yapısı**|
|:- |
|![Aspose.Diagram Nesne Modeli'nin üst düzey yapısı](diagram-classes.png)|

Yukarıdaki şekilden de görebileceğiniz gibi, nesne modelinin kökü Diagram nesnesidir. Giriş amacıyla aşağıda nesnelerin birkaçının kısa bir açıklaması verilmiştir.

#### **Sayfa Koleksiyonu/Sayfa**

Diagram nesnesi, bir Diagram'deki tüm Page nesnelerinin koleksiyonunu temsil eden PageCollection'ı içerir.

#### **ŞekilToplama/Şekil**

Page nesnesi, bir Page içindeki tüm Shape nesnelerinin koleksiyonunu temsil eden ShapeCollection'ı içerir. Şekil nesnesi, bir Kalıp, Sayfa veya grup şekil öğesinde bir şekli tanımlayan öğeler içerir.

#### **BağlanToplama/Bağlan**

Page nesnesi, bir Page içindeki tüm Connect nesnelerinin koleksiyonunu temsil eden ConnectCollection'ı içerir. Bağlan nesnesi, bir kuruluş şemasındaki çizgi ve kutu gibi bir çizimdeki iki şekil arasındaki bağlantıyı temsil eder.

#### **StyleSheetCollection/StyleSheet**

Belgede tanımlanmış bir stili temsil eder.

#### **MasterCollection/Master**

Belge için bir kalıp tanımlayan öğeleri içerir. Kalıp, çizimler oluşturmak için tekrar tekrar kullandığınız bir kalıp üzerindeki şekildir. Bir kalıbı çizim sayfasına bir şekil sürüklediğinizde, şekil o kalıbın bir örneği haline gelir ve kalıbın yerel bir kopyası belgeye dahil edilir.

#### **Döküman özellikleri**

Belgenin başlığı, yazarı vb. gibi belge özellik öğelerini içerir.

#### **Üstbilgi Altbilgi**

Bir belgenin üstbilgisi ve altbilgisi için öğeler içerir.

#### **Vba Projesi**

VBA projesini temsil eder.

#### **TemaKoleksiyon/Tema**

Dinamik tema, renk, yazı tipi, dolgu, çizgi özellikleri ve efekt özelliklerini belirten özellikleri tanımlar.

#### **Doldurmak**

Desen, ön plan rengi ve arka plan rengi dahil olmak üzere şekil ve şeklin alt gölgesi için geçerli dolgu biçimlendirme değerlerini içerir.

#### **Astar**

Desen, ağırlık ve renk gibi bir şeklin çizgi niteliklerini kontrol eden öğeleri içerir. Bu öğeler, satır uçlarının biçimlendirilip biçimlendirilmediğini (örneğin, bir ok başıyla), satır sonu biçimlerinin boyutunu, satıra uygulanan yuvarlama dairesinin yarıçapını ve satır başlığı stilini (yuvarlak veya kare) belirler.

#### **Geomlar**

Geom öğelerinin bir koleksiyonunu içerir.

#### **karakterler**

Şeklin metin stillerini içeren bir Char nesnesi koleksiyonu içerir.

#### **Metin**

Bir şeklin metnini içerir.

#### **XForm**

Bir şekil hakkında genel konumlandırma bilgilerini belirten öğeler içerir.

#### **MetinXForm**

Bir şeklin metin bloğu hakkında konumlandırma bilgilerini belirten öğeler içerir.

#### **Köprü Koleksiyonu/Köprü**

Köprü nesnesi, bir şekil veya çizim sayfası ile başka bir çizim sayfası, başka bir dosya veya Web sitesi arasında çoklu atlamalar oluşturmak için öğeler içerir.

#### **Ana Şekil**

Bu öznitelik, yalnızca bir grup şeklinin üyesi olan şekillerde bulunabilir ve grup, bir ana örneğin örneğidir. Öznitelik, ana öğede karşılık gelen alt şekle başvuran bir kimlik içerir.

#### **AlanToplama/Alan**

Alan nesnesi, şeklin metnine eklenen işlevleri ve formülleri belirten öğeler içerir.
