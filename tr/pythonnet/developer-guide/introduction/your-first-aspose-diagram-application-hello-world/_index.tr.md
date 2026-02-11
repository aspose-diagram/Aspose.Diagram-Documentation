---
title: İlk Başvurunuz Aspose.Diagram - Hello World
type: docs
weight: 30
url: /tr/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

Bu yeni başlayanlar için konu, geliştiricilerin Aspose.Diagram' basit API'i kullanarak basit bir ilk uygulamayı (Hello World) nasıl oluşturabileceklerini gösterir. Uygulama, sayfada Hello World sözcükleriyle bir Microsoft Visio dosyası oluşturur.

{{% /alert %}}

### **Hello World Uygulamasını Oluşturma**

Hello World uygulamasını Aspose.Diagram API kullanarak oluşturmak için:

1. Workbook sınıfının bir örneğini oluşturun.
1. Lisansı uygula:
 1. Bir lisans satın aldıysanız, Aspose.Diagram'in tüm işlevlerine erişmek için uygulamanızdaki lisansı kullanın.
 1. Bileşenin değerlendirme sürümünü kullanıyorsanız (Aspose.Diagram'i lisanssız kullanıyorsanız), bu adımı atlayın.
1. Yeni bir Microsoft Visio dosyası oluşturun veya metin eklemek/güncellemek istediğiniz mevcut bir dosyayı açın.
1.  kelimeleri ekle**Hello World!** erişilen sayfaya
1. Değiştirilen Microsoft Visio dosyasını oluşturun.

Aşağıdaki örnekler yukarıdaki adımları göstermektedir.

#### **Diagram oluşturma**

Aşağıdaki örnek, sıfırdan yeni bir diagram oluşturur, "Hello World!" ilk sayfada ve dosyayı kaydeder.

**Yeni visio dosyası oluştur** 

![yapılacaklar:resim_alternatif_Metin](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **Mevcut Bir Dosyayı Açmak**

Aşağıdaki örnek, mevcut bir Microsoft Visio şablon dosyasını açar, "Hello World!" ilk sayfada ve diagram'i yeni bir dosya olarak kaydeder.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

diagram = Diagram(os.path.join(sourceDir, "Basic Shapes.vss"))

#// Add a new hello world rectangle shape
shapeId = diagram.add_shape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.pages[0].shapes.get_shape(shapeId)
shape.text.value.add(Txt("Hello World"))

#// Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}

