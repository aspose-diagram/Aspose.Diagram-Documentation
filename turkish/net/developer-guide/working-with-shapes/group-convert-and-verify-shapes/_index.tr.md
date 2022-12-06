---
title: Şekilleri Gruplandırın, Dönüştürün ve Doğrulayın
type: docs
weight: 80
url: /tr/net/group-convert-and-verify-shapes/
description: Bu bölümde şekillerin Aspose.Diagram ile nasıl gruplandırılacağı açıklanmaktadır.
---
## **Visio Çiziminde Birden Fazla Şekli Birlikte Gruplandırın**
Aspose.Diagram API, geliştiricilerin şekilleri bir arada gruplandırmasına ve hepsini aynı anda taşımasına olanak tanır. Bir gruptaki her şekil benzersiz bir kimliğe sahiptir ve kendi özelliklerine sahiptir. Bir şekil grubunun biçimlendirmesini değiştirdiğimizde, her şekle yeni özellik atar.
### **Şekiller Nasıl Gruplandırılır?**
 tarafından sunulan Grup yöntemi[Şekil Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, şekilleri birlikte gruplandırmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. şekillerin bir dizisini başlattı
1. kimliğe göre belirli bir şekil elde edin.
1. kimliğe göre başka bir özel şekil elde edin.
1. diziye şekiller atayın.
1. Group yöntemini çağırarak şekilleri gruplandırın.
1. kaydet diagram
#### **Grup Şekilleri Programlama Örneği**
Aspose.Diagram for .NET API'i kullanarak şekilleri gruplandırmak için .NET uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
## **Visio Şeklini Diğer Dosya Biçimlerine Dönüştürme**
Aspose.Diagram for .NET API, geliştiricilerin tek bir Visio şeklini desteklenen diğer herhangi bir dosya biçimine dönüştürmesine olanak tanır. Bu yazıda, diğer tüm Visio şekillerini sayfadan kaldırıyoruz ve sayfa ayarını kaynak Şekil boyutuna göre özelleştiriyoruz.
### **Belirli Bir Şekli Dönüştürme Visio**
 Geliştiriciler, bir Visio şeklini şu şekilde PDF, HTML, Image, SVG ve SWF'e dönüştürebilir.**Visio kaydetme seçeneklerini belirleme**.
Bu örnek kod aşağıdaki gibi çalışır:

1. Bir kaynak yükleyin Visio.
1. Belirli bir sayfa alın.
1. Arka plan sayfasını kaldırın.
1. Kimlikleri ve adları tutan tüm şekillerden oluşan bir karma tablo oluşturun.
1. Hash tablosunu yineleyin
1. Belirli bir şekil dışında tüm şekilleri Visio sayfasından kaldırın.
1. Sayfa boyutunu ayarlayın.
1. Visio sayfasını desteklenen herhangi bir dosya biçiminde kaydedin.
#### **Şekil Programlama Örneği Dönüştür**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
### **Visio Şeklini PDF'e dönüştür**
Shape sınıfının ToPdf yöntemi, bir şekli PDF biçimine dönüştürmeye olanak tanır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Visio Şeklini HTML'e dönüştür**
Shape sınıfının ToHTML yöntemi, bir şeklin HTML biçimine dönüştürülmesine izin verir.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **İki Visio Şeklin Bağlantılı veya Yapıştırılmış Olduğunu Doğrulayın**
 Aspose.Diagram for .NET API, geliştiricilerin iki Visio şeklinin yapıştırıldığını veya bağlantılı olduğunu doğrulamasına olanak tanır. Daha önce, bu yardım konularında iki şekli nasıl birleştirebileceğimizi veya yapıştırabileceğimizi gördük:[Ekle ve Bağla Visio Şekiller](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) ve[Kabın İçindeki Tutkal Şekilleri](/diagram/tr/net/working-with-shapes-gluing/).
### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması**
 bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, iki şeklin yapıştırılmış mı yoksa bağlantılı mı olduğunu belirlemek için IsGlued ve IsConnected özelliklerini sunar.
#### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması Programlama Örneği**
Aşağıdaki kod parçası, iki şeklin bağlantılı mı yoksa yapıştırılmış mı olduğunu doğrular.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **Visio Şeklinin bir Şekil Grubunda Olup Olmadığını Doğrulayın**
Aspose.Diagram for .NET API, geliştiricilerin Visio şeklinin bir grup şekil içinde olup olmadığını doğrulamasını sağlar.
### **Şekil Grubunda Şeklin Doğrulanması**
bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, Visio şeklinin bir grup şeklinde olup olmadığını belirlemek için IsInGroup özelliklerini sunar.
#### **Şekiller Grubu Programlama Örneğinde Şeklin Doğrulanması**
Aşağıdaki kod parçası, şeklin bir grup şeklinde olup olmadığını doğrular.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
