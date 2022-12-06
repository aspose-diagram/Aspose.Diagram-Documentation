---
title: Yorumlarla Çalışmak
type: docs
weight: 210
url: /tr/java/working-with-comments/
---
## **Visio'de Sayfa Düzeyinde Yorum ekleyin**
Aspose.Diagram for Java API, geliştiricilerin Visio çiziminin bir sayfasında herhangi bir yere yorum eklemesine olanak tanır.
### **Yorum ekle**
Page sınıfı tarafından sunulan addComment yöntemi, bir çizim sayfasına yorum eklemenize olanak tanır. Bir yorum dizesiyle birlikte X ve Y koordinatlarını alır.

 Microsoft Visio kullanıcıları, sayfanın sol üst köşesinde bir simge ile sunulan tüm sayfaya yorum ekler. Geliştiriciler şunları yapabilir:[Visio'de sayfa düzeyinde yorumlar ekleyin](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API ayrıca Visio'deki sayfa düzeyindeki yorumu değiştirmeyi destekler.
#### **Yorum Programlama Örneği Ekle**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Visio Diagram'de bir Sayfa Düzeyinde Yorum düzenleyin**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, sayfanın sol üst köşesinde bir simge ile gösterilen Visio çizim sayfasındaki sayfa düzeyinde yorumu değiştirme desteğine sahiptir.
### **Yorumu Düzenle**
Annotation sınıfı tarafından sunulan Comment özelliği, geliştiricilerin Visio çizim sayfasındaki yorumları düzenlemesine olanak tanır.
#### **Yorum Programlama Örneği Düzenle**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **Visio Çiziminde Şekil Düzeyinde Yorum Ekleme**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, geliştiricilerin Visio çizimindeki şekle yorum eklemesine olanak tanır.
### **Yorum ekle**
Page sınıfı tarafından sunulan aşırı yüklenmiş bir addComment yöntemi, bir Shape sınıfı örneğini ve yorumun metin dizesini alır.
#### **Yorum Programlama Örneği Ekle**
**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
