---
title:  Visio'i diğer formatlara dönüştürün
linktitle:  Visio'i diğer formatlara dönüştürün
type: docs
weight: 40
url: /tr/java/convert-visio-to-other-files/
description: Bu konu, Aspose.Diagram'in Visio'i SVG,XPS,XML,XAML biçimlerine dönüştürmeye nasıl izin verdiğini gösterir. VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM'i SVG,XPS,15,0761,XML'ye dönüştürün.
---
## **XML'e dışa aktarma**
 Bu makalede, bir Microsoft Visio diagram kullanarak XML'e nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- VDX, bir XML diagram tanımlar.
- VTX, bir XML şablonu tanımlar.
- VSX, bir XML şablonunu tanımlar.

 bu[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' yapıcıları bir diagram'i okur ve Save yöntemi, bir diagram'i farklı bir dosya biçiminde kaydetmek veya dışa aktarmak için kullanılır. Bu makaledeki kod parçacıkları, bir Visio dosyasını şuraya kaydetmek için Kaydet yönteminin nasıl kullanılacağını gösterir:[VDX](/diagram/tr/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/tr/java/how-to-convert-a-visio-diagram/) ve[VSX](/diagram/tr/java/how-to-convert-a-visio-diagram/).

Aşağıdaki resim, aşağıdaki kod parçacıklarında dışa aktarılan diagram'i göstermektedir. Dışa aktarılan dosya, her kod parçacığından önce gösterilir.

**A Microsoft Visio diagram ihraç edilmek üzere.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/XWajazh.png)
### **VSD'den VDX'e dışa aktarma**
VDX, diyagramları Microsoft Visio dışındaki ürünlerin okuyabileceği bir biçimde kaydetmenizi sağlayan şema tabanlı bir XML dosya biçimidir. Yazılım uygulamaları arasında diyagramları aktarmak ve düzenlenebilir verileri tutmak için kullanışlı bir formattır.

Bir VSD diagram'i VDX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VDX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

**Dışa aktarılan VDX dosyası.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/OJ1jpgh.png)
### **VSD'den VSX'e dışa aktarma**
VSX, diagram'in oluşturulduğu temel nesneler olan şablonları tanımlamak için bir XML formatıdır. Visio dosyası VSX'e dönüştürüldüğünde, yalnızca şablonlar dışa aktarılır.

Bir VSD diagram'i VSX'e aktarmak için:

- Diagram sınıfının bir örneğini oluşturun.
- Visio çizim dosyasını VSX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

Aşağıdaki görüntü VSX çıktı dosyasını göstermektedir. diagram'in kendisinin değil, diagram'de kullanılan şablonların dışa aktarıldığını unutmayın.

**Dışa aktarılan VSX dosyası.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/gkZrxCN.png)
### **VSD'i VTX'e aktar**
TVX, bir şablon dosyasının XML temsilidir ve belgenin ayarlarını saklar.

Bir VSD diagram'i VTX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VTX biçiminde yazmak için diagram sınıfının Save yöntemini çağırın.

Aşağıdaki görüntü VTX çıktı dosyasını göstermektedir.

**Çıktı VTX dosyası.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/E6pUvGD.jpg)
### **XML Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXML-ExportToXML.java" >}}
## **XPS'e aktarılıyor**
 Bu makalede, bir Microsoft Visio diagram'in XPS kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

Bu makaledeki kod parçacıkları aşağıdaki diagram'i girdi olarak alır. Diğer diagram formatlarını da kullanabilirsiniz (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX veya VSX).

**Kaynak belge.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/P3gaA34.png)

VSD diagram'i XPS'e dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfının Save yöntemini çağırın ve çıkış formatı olarak XPS'i ayarlayın.

Aşağıdaki görüntü XPS çıktı dosyasını göstermektedir.

**Çıkış XPS.**

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/1ESRxSy.png)
### **XPS Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXPS-ExportToXPS.java" >}}
## **Diagram'i SVG'e dışa aktarma**
 Bu makalede, bir Microsoft Visio diagram'in SVG'e (Ölçeklenebilir Vektör Grafikleri) kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

VSD diagram'i SVG'e aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Sınıfın Save yöntemini çağırın ve dışa aktarma formatı olarak SVG'i ayarlayın.
### **Diagram'i SVG'e Aktarma Programlama Örneği**
Kod örnekleri, Java kullanarak bir diagram'in SVG'e nasıl aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToSVG-ExportToSVG.java" >}}
## **Diagram'i XAML'e dışa aktarma**
Bu makalede, bir Microsoft Visio diagram'in XAML'e (Genişletilebilir Uygulama İşaretleme Dili) kullanılarak nasıl dışa aktarılacağı açıklanmaktadır.[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Kullan[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) diagram dosyalarını okumak için 'class' yapıcısı ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemi.

Bir VSD diagram'i XAML'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Sınıfın Save yöntemini çağırın ve dışa aktarma formatı olarak XAML'i ayarlayın.
### **XAML Programlama Örneğine Aktarma**
Kod örneği, Java kullanarak bir diagram'in XAML'e nasıl aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToXAML-ExportToXAML.java" >}}

## **Dönüştür Visio Seçici Şekillerle Çizim**
Aspose.Diagram API'i kullanan geliştiriciler, bir Visio çizimini desteklenen herhangi bir formata dönüştürmek için bir grup şekil seçebilirler. RenderingSaveOptions sınıfı, şekil grubunu korumak için bir Shapes üyesi sunar. Her kaydetme seçeneği sınıfı, RenderingSaveOptions sınıfının genişletilmiş biçimidir.

Bir Visio çizimini seçici şekillerle dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Ayarları burada anlatıldığı gibi belirtmek için herhangi bir SaveOption sınıfının bir örneğini oluşturun:[Visio Kaydetme Seçeneklerini Belirtin](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. Diagram sınıf nesnesinin kaydetme yöntemini çağırın ve kaydetme seçeneği sınıf nesnesini parametre olarak iletin.
### **Dönüştür Visio Seçici Şekillerle Çizim Programlama Örneği**
Kod örneği, bir çizimin seçici Visio şekillerle nasıl dışa aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ConvertVisioWithSelectiveShapes.Java" >}}