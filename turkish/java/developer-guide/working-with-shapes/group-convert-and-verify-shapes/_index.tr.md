---
title: Şekilleri Gruplandırın, Dönüştürün ve Doğrulayın
type: docs
weight: 50
url: /tr/java/group-convert-and-verify-shapes/
---
## **Visio Çiziminde Birden Fazla Şekli Birlikte Gruplandırın**
Aspose.Diagram API, geliştiricilerin şekilleri bir arada gruplandırmasına ve hepsini aynı anda taşımasına olanak tanır. Bir gruptaki her şekil benzersiz bir kimliğe sahiptir ve kendi özelliklerine sahiptir. Bir şekil grubunun biçimlendirmesini değiştirdiğimizde, her şekle yeni özellik atar.
### **Şekiller Nasıl Gruplandırılır?**
ShapeCollection sınıfı tarafından sunulan Group yöntemi, şekilleri birlikte gruplandırmak için kullanılabilir.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir numune yükleyin diagram.
1. şekillerin bir dizisini başlattı
1. kimliğe göre belirli bir şekil elde edin.
1. kimliğe göre başka bir özel şekil elde edin.
1. diziye şekiller atayın.
1. Group yöntemini çağırarak şekilleri gruplandırın.
1. kaydet diagram
#### **Grup Şekilleri Programlama Örneği**
Aspose.Diagram for Java API'i kullanarak şekilleri gruplandırmak için Java uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GroupShapes-GroupShapes.java" >}}
## **Visio Şeklini Diğer Dosya Biçimlerine Dönüştürme**
Aspose.Diagram for Java API, geliştiricilerin tek bir Visio şeklini desteklenen diğer herhangi bir dosya biçimine dönüştürmesine olanak tanır. Bu yazıda, diğer tüm Visio şekillerini sayfadan kaldırıyoruz ve sayfa ayarını kaynak Şekil boyutuna göre özelleştiriyoruz.
### **Belirli Bir Şekli Dönüştürme Visio**
 Geliştiriciler, bir Visio şeklini şu şekilde PDF, HTML, Image, SVG ve SWF'e dönüştürebilir.[Visio kaydetme seçeneklerini belirleme]().
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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.java" >}}
### **Visio Şeklini PDF'e dönüştür**
Shape sınıfının ToPdf yöntemi, bir şekli PDF biçimine dönüştürmeye olanak tanır.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Visio Şeklini HTML'e dönüştür**
Shape sınıfının ToHTML yöntemi, bir şeklin HTML biçimine dönüştürülmesine izin verir.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}} 
## **İki Visio Şeklin Bağlantılı veya Yapıştırılmış Olduğunu Doğrulayın**
 Aspose.Diagram for Java API, geliştiricilerin iki Visio şeklinin yapıştırıldığını veya bağlantılı olduğunu doğrulamasına olanak tanır. Daha önce, bu yardım konularında iki şekli nasıl birleştirebileceğimizi veya yapıştırabileceğimizi gördük:[Ekle ve Bağla Visio Şekiller](/diagram/tr/java/add-and-connect-visio-shapes/) ve[Kabın İçindeki Tutkal Şekilleri](/diagram/tr/java/working-with-shapes-gluing/).
### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması**
 bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, iki şeklin yapıştırılmış mı yoksa bağlantılı mı olduğunu belirlemek için IsGlued ve IsConnected özelliklerini sunar.
#### **Bağlı veya Yapıştırılmış Şekillerin Doğrulanması Programlama Örneği**
Aşağıdaki kod parçası, iki şeklin bağlantılı mı yoksa yapıştırılmış mı olduğunu doğrular.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.java" >}}
## **Visio Şeklinin bir Şekil Grubunda Olup Olmadığını Doğrulayın**
Aspose.Diagram for Java API, geliştiricilerin Visio şeklinin bir grup şekil içinde olup olmadığını doğrulamasını sağlar.
### **Şekil Grubunda Şeklin Doğrulanması**
Shape sınıfı, Visio şeklinin bir grup şeklinde olup olmadığını belirlemek için IsInGroup özellikleri sunar.
#### **Şekiller Grubu Programlama Örneğinde Şeklin Doğrulanması**
Aşağıdaki kod parçası, şeklin bir grup şeklinde olup olmadığını doğrular.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.java" >}}

{{% alert color="primary" %}} 

 Soru ve önerilerinizi şu adrese bekliyoruz:[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Derhal cevap vereceğiz.

{{% /alert %}}
