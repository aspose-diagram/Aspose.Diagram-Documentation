---
title:  Visio'i diğer formatlara dönüştürün
linktitle:  Visio'i diğer formatlara dönüştürün
type: docs
weight: 40
url: /tr/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML ,XAML birkaç satır kodla.
---
**[Dışa aktarılacak bir Microsoft Visio diagram.](ExportToXML.vsd)**

## **XML'e dışa aktarma**
Bu makalede, Python için Java aracılığıyla Aspose.Diagram kullanılarak bir Microsoft Visio diagram'in XML'e nasıl aktarılacağı açıklanmaktadır.

- VDX, bir XML diagram tanımlar.
- VTX, bir XML şablonu tanımlar.
- VSX, bir XML şablonunu tanımlar.

Diagram sınıfının yapıcıları bir diagram'i okur ve Save yöntemi, bir diagram'i farklı bir dosya biçiminde kaydetmek veya dışa aktarmak için kullanılır. Bu makaledeki kod parçacıkları, bir Visio dosyasını VDX, VTX ve VSX biçimlerine kaydetmek için Kaydet yönteminin nasıl kullanılacağını gösterir.

### **VSD'den VDX'e dışa aktarma**
VDX, diyagramları Microsoft Visio dışındaki ürünlerin okuyabileceği bir biçimde kaydetmenizi sağlayan şema tabanlı bir XML dosya biçimidir. Yazılım uygulamaları arasında diyagramları aktarmak ve düzenlenebilir verileri tutmak için kullanışlı bir formattır.

Bir VSD diagram'i VDX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VDX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

### **VSD'den VSX'e dışa aktarma**
VSX, diagram'in oluşturulduğu temel nesneler olan şablonları tanımlamak için bir XML formatıdır. Visio dosyası VSX'e dönüştürüldüğünde, yalnızca şablonlar dışa aktarılır.

Bir VSD diagram'i VSX'e aktarmak için:

- Diagram sınıfının bir örneğini oluşturun.
- Visio çizim dosyasını VSX'e yazmak için Diagram sınıfının Save yöntemini çağırın.

Aşağıdaki görüntü VSX çıktı dosyasını göstermektedir. diagram'in kendisinin değil, diagram'de kullanılan şablonların dışa aktarıldığını unutmayın.

### **VSD'i VTX'e aktar**
TVX, bir şablon dosyasının XML temsilidir ve belgenin ayarlarını saklar.

Bir VSD diagram'i VTX'e aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Visio çizim dosyasını VTX biçiminde yazmak için diagram sınıfının Save yöntemini çağırın.

Aşağıdaki görüntü VTX çıktı dosyasını göstermektedir.

### **XML Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXML.py" >}}

## **XPS'e Aktarma**
Bu makalede, Python için Java aracılığıyla Aspose.Diagram kullanılarak bir Microsoft Visio diagram'in XPS'ye nasıl aktarılacağı açıklanmaktadır.
diagram dosyalarını okumak için Diagram sınıfının yapıcısını ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın.

Bu makaledeki kod parçacıkları aşağıdaki diagram'i girdi olarak alır. Diğer diagram formatlarını da (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX veya VSX) kullanabilirsiniz.

VSD diagram'i XPS'ye dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Diagram sınıfının Save yöntemini çağırın ve çıkış formatı olarak XPS'yi ayarlayın.

Aşağıdaki görüntü çıktı XPS dosyasını göstermektedir.

### **XPS Programlama Örneğine Aktarma**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **Diagram'i SVG'ye dışa aktarma**
Bu makalede, Python için Aspose.Diagram kullanılarak Java yoluyla bir Microsoft Visio diagram'in SVG'ye (Ölçeklenebilir Vektör Grafikleri) nasıl aktarılacağı açıklanmaktadır.

diagram dosyalarını okumak için Diagram sınıfının yapıcısını ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın.

VSD diagram'i SVG'ye aktarmak için aşağıdaki adımları gerçekleştirin:

1. Diagram sınıfının bir örneğini oluşturun.
1. Sınıfın Save yöntemini çağırın ve dışa aktarma formatı olarak SVG'yi ayarlayın.

### **Diagram'i SVG Programlama Örneğine Aktarma**
Kod örnekleri, diagram'in Java kullanılarak SVG'ye nasıl aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **Diagram'i XAML'ye dışa aktarma**
Bu makalede, Python için Aspose.Diagram kullanılarak Java yoluyla bir Microsoft Visio diagram'in XAML'ye (Genişletilebilir Uygulama İşaretleme Dili) nasıl aktarılacağı açıklanmaktadır.

diagram dosyalarını okumak için Diagram sınıfının yapıcısını ve diagram'i desteklenen herhangi bir görüntü formatına dışa aktarmak için Save yöntemini kullanın.

Bir VSD diagram'i XAML'ye dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Sınıfın Save yöntemini çağırın ve XAML'yi dışa aktarma formatı olarak ayarlayın.

### **XAML Programlama Örneğine Aktarma**
Kod örneği, diagram'in Java kullanılarak XAML'ye nasıl aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXAML.py" >}}

## **Dönüştür Visio Seçici Şekillerle Çizim**
Aspose.Diagram API'i kullanan geliştiriciler, bir Visio çizimini desteklenen herhangi bir formata dönüştürmek için bir grup şekil seçebilirler. RenderingSaveOptions sınıfı, şekil grubunu korumak için bir Shapes üyesi sunar. Her kaydetme seçeneği sınıfı, RenderingSaveOptions sınıfının genişletilmiş biçimidir.

Bir Visio çizimini seçici şekillerle dışa aktarmak için:

1. Diagram sınıfının bir örneğini oluşturun.
1. Ayarları anlatımlı olarak belirtmek için herhangi bir SaveOption sınıfının bir örneğini oluşturun
1. Diagram sınıf nesnesinin kaydetme yöntemini çağırın ve kaydetme seçeneği sınıf nesnesini parametre olarak iletin.

### **Dönüştür Visio Seçici Şekillerle Çizim Programlama Örneği**
Kod örneği, bir çizimin seçici Visio şekillerle nasıl dışa aktarılacağını gösterir.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ConvertVisioWithSelectiveShapes.py" >}}