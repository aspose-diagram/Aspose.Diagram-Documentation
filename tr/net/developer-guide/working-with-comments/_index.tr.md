---
title: Yorumlarla Çalışmak
type: docs
weight: 220
url: /tr/net/working-with-comments/
description: Bu sayfa, Aspose.Diagram kitaplığıyla nasıl yorum ekleneceğini veya düzenleneceğini açıklar.
---
## **Visio'de Sayfa Düzeyinde Yorum ekleyin**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API, geliştiricilerin Visio çizim sayfasında herhangi bir yere yorum yerleştirmesine olanak tanır.
### **Yorum ekle**
 Tarafından sunulan AddComment yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf, geliştiricilerin bir çizim sayfasına yorum eklemesine izin verir. Bir yorum dizesiyle birlikte X ve Y koordinatlarını alır.
#### **Yorum Programlama Örneği Ekle**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.Save(dataDir + "AddComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Diagram'de bir Sayfa Düzeyinde Yorum düzenleyin**
 Microsoft Visio kullanıcıları, sayfanın sol üst köşesinde bir simge ile sunulan tüm sayfaya yorum ekler. Geliştiriciler şunları yapabilir:[Visio'de sayfa düzeyinde yorumlar ekleyin](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API ayrıca Visio'deki sayfa düzeyindeki yorumu değiştirmeyi destekler.
### **Yorumu Düzenle**
 Tarafından sunulan Comment özelliği,[Dipnot](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class, geliştiricilerin Visio çizim sayfasındaki yorumları düzenlemesine olanak tanır.
#### **Yorum Programlama Örneği Düzenle**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get collection of the annotations
AnnotationCollection annotations = diagram.Pages.GetPage("Page-1").PageSheet.Annotations;

// Iterate through the annotations
foreach (Annotation annotation in annotations)
{
    string comment = annotation.Comment.Value;
    comment += "Updation mark";
    annotation.Comment.Value = comment;
}
// Save Visio
diagram.Save(dataDir + "EditComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visio Çiziminde Şekil Düzeyinde Yorum Ekleme**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API, geliştiricilerin Visio çizimindeki şekle yorum eklemesine olanak tanır.
### **Yorum ekle**
Tarafından sunulan aşırı yüklenmiş bir AddComment yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page)class, Shape sınıfı örneğini ve yorumun metin dizesini alır.
#### **Yorum Programlama Örneği Ekle**
**C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
