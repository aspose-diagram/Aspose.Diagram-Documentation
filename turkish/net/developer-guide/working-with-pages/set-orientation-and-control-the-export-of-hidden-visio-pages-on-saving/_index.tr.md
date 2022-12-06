---
title: Yönlendirmeyi Ayarlayın ve Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin
type: docs
weight: 20
url: /tr/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: Bu bölümde sayfa düzeninin Aspose.Diagram ile nasıl ayarlanacağı açıklanmaktadır.
---
## **Visio Sayfa Düzenini Dikey veya Yatay olarak değiştirme**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API, geliştiricilerin Visio çizim sayfasının yönünü programlı olarak ayarlamasına olanak tanır. Bu yardım konusu, bu görevin nasıl gerçekleştirileceğini açıklar.

 Aspose.Diagram for .NET API'de var[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Visio çizim sayfasını temsil eden sınıf. Page sınıfı tarafından sunulan PageSheet özelliği ayrıca yazdırma özelliklerini de gösterir. Yazdırma özelliklerinin PrintPageOrientation alanı, sayfayı döndürmeye izin verir. Dikey, Yatay ve yazıcıdaki ile aynı olmak üzere üç seçenek sunar. PrintPageOrientation alanı, Aspose.Diagram API kullanılarak programlı olarak ayarlanabilir.

Bu örnek şu şekilde çalışır:

1. Mevcut bir Visio diagram'i Diagram sınıf nesnesine yükleyin.
1. Visio sayfasını ayıklayın
1. Yönünü Dikey, Yatay veya yazıcıdakiyle aynı olarak ayarlayın.
1. Visio diagram'i kaydedin.
### **Oryantasyon Programlama Örneği Ayarla**
Aşağıdaki kod örneği, Visio sayfasının yönünün nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Kaydederken Gizli Visio Sayfalarının Dışa Aktarılmasını Kontrol Edin**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API, geliştiricilerin diagram'i PDF, HTML, Görüntü (PNG, JPEG, GIF), SVG ve XPS dosyalarına kaydederken gizli Visio sayfalarını dahil etmesine veya hariç tutmasına olanak tanır. Hatta Aspose.Diagram API'i kullanarak Visio sayfayı gizleyebilirler çünkü seçeneği ShapeSheet sayfasındaki UIVisibility hücresi aracılığıyla zaten mevcuttur.
### **Visio Diagram'de bir Sayfayı Gizle ve Dışa Aktarma Seçeneğini Ayarla**
 Aspose.Diagram for .NET API'de var[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Visio çizim sayfasını temsil eden sınıf. Page sınıfı tarafından sunulan PageSheet özelliği, sayfa özelliklerini de gösterir. Sayfa özelliklerinin UIVisibility alanı, sayfanın gizlenmesine olanak tanır. Geliştiriciler daha sonra SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions ve PdfSaveOptions sınıflarına eklenen ExportHiddenPage özelliğini kullanabilir.
#### **PDF için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i PDF biçiminde kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **HTML için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i HTML biçimine kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Görüntü için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i görüntü formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **SVG için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i SVG biçimine kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **XPS için Dışa Aktarma Seçeneğini Ayarlayın**
Aşağıdaki kod, bir diagram'i XPS biçimine kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
