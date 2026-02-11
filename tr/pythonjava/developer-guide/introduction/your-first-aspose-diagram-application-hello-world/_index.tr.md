---
title: İlk Başvurunuz Aspose.Diagram - Hello World
type: docs
weight: 30
url: /tr/python-java/your-first-aspose-diagram-application-hello-world/
description: Bu sayfada Aspose.Diagram kitaplığı ile ilk uygulamanın nasıl oluşturulacağı açıklanmaktadır.
---
{{% alert color="primary" %}}

Bu öğretici, Aspose.Diagram' basit API'i kullanarak ilk uygulamanın (Hello World) nasıl oluşturulacağını gösterir. Bu basit uygulama, belirli bir Sayfada 'Hello World' metniyle bir Microsoft Visio dosyası oluşturur.

{{% /alert %}}

## **Hello World Uygulamasını Oluşturma**

Aşağıdaki adımlar, Aspose.Diagram API'i kullanarak Hello World uygulamasını oluşturur:

1. Diagram sınıfının bir örneğini oluşturun.
1. Lisansı uygula:
 1. Bir lisans satın aldıysanız, Aspose.Diagram'in tüm işlevlerine erişmek için uygulamanızdaki lisansı kullanın.
 1. Bileşenin değerlendirme sürümünü kullanıyorsanız (Aspose.Diagram'i lisanssız kullanıyorsanız), bu adımı atlayın.
1. Yeni bir Visio dosyası oluşturun veya mevcut bir Visio dosyasını açın.
1. Yeni bir metin kutusu oluşturun.
1.  kelimeleri ekle**Hello World!** bir metin kutusuna.
1. Değiştirilen Microsoft Visio dosyasını oluşturun.

Yukarıdaki adımların uygulanması aşağıdaki örneklerde gösterilmektedir.

### **Kod Örneği: Yeni Diagram Oluşturup Hello World Yazıyor!**

Aşağıdaki örnek, " adlı mevcut bir Microsoft Visio şablon dosyasını açar.[Basic_Shapes.vss](Basic_Shapes.vss)", ilk sayfaya "Hello World!" yazısını girer ve diagram'i kaydeder.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Basic_Shapes.vss")

# Add a new hello world rectangle shape
shapeId = diagram.addShape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.getPages().getPage(0).getShapes().getShape(shapeId)
shape.getText().getValue().add(Txt("Hello World"))

# Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
