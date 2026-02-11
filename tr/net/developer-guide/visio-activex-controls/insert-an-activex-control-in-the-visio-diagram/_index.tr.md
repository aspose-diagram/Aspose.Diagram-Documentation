---
title: Visio Diagram'e bir ActiveX Denetimi ekleyin
type: docs
weight: 10
url: /tr/net/insert-an-activex-control-in-the-visio-diagram/
description: Bu sayfa, Aspose.Diagram kitaplığıyla bir activeX Denetiminin nasıl ekleneceğini açıklar.
---
{{% alert color="primary" %}}

 Geliştiriciler, ActiveX denetimlerini doğrudan Microsoft Visio çizimlerine ekleyerek Visio diagram'i etkileşimli hale getirebilir.[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Bir ActiveX Kontrol Programlama Örneği Ekleme**
[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, AddActiveXControl yöntemini sunar ve geliştiricilerin komut düğmesi, birleşik giriş kutusu, onay kutusu, liste kutusu, metin kutusu, döndürme düğmesi, radyo düğmesi, etiket, resim, geçiş düğmesi ve kaydırma çubuğu gibi her türlü ActiveX denetimini eklemesine izin verir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// Save diagram
diagram.Save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
