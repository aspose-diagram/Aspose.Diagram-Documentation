---
title: Visio Diagram'e bir ActiveX Denetimi ekleyin
type: docs
weight: 10
url: /tr/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 Geliştiriciler, ActiveX denetimlerini doğrudan Microsoft Visio çizimlerine ekleyerek Visio diagram'i etkileşimli hale getirebilir.[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Bir ActiveX Kontrol Programlama Örneği Ekleme**
[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class, addActiveXControl yöntemini sunar ve geliştiricilerin komut düğmesi, birleşik giriş kutusu, onay kutusu, liste kutusu, metin kutusu, döndürme düğmesi, radyo düğmesi, etiket, resim, geçiş düğmesi ve kaydırma çubuğu gibi her türlü ActiveX denetimini eklemesine izin verir.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertanActiveControl.class) + "VisioActiveXControls/";
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);
// Save diagram
diagram.save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
