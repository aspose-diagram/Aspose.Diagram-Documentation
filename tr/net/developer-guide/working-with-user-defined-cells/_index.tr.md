---
title: Kullanıcı Tanımlı Hücrelerle Çalışma
type: docs
weight: 150
url: /tr/net/working-with-user-defined-cells/
description: Bu bölümde, visio şekillerinin Kullanıcı tanımlı hücrelerinin Aspose.Diagram ile nasıl okunacağı açıklanmaktadır.
---
## **Visio Şekillerinin Kullanıcı Tanımlı Hücrelerini Oku**
 Kullanıcılar, ek bilgileri görüntülemek için şekillere metin alanları ekler.**Kullanıcı Tanımlı Hücreler** bu alanların tek dalıdır ve bu dal, şeklin ShapeSheet'indeki Kullanıcı Tanımlı Hücreler bölümünün Değer hücresine girilen bilgileri kullanır. Geliştiriciler, kullanarak tüm kullanıcı tanımlı hücreleri ekleyebilir ve okuyabilir[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Kullanıcı Tanımlı Hücre Alanlarını Alın**
 Şunun tarafından açığa çıkarılan kullanıcı koleksiyonu:[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class Aspose.Diagram.User nesnesini destekler. Bu özellik, şeklin ShapeSheet'inin Kullanıcı Tanımlı Hücreler bölümünde bulunan Visio şeklinin kullanıcı tanımlı hücrelerini okumak için kullanılabilir.

![yapılacaklar:resim_alternatif_Metin](working-with-user-defined-cells_1.png)
#### **Hücreleri Programlama Örneği Al**
Aşağıdaki kod parçası, geliştiricilerin kullanıcı tanımlı hücre alanlarını okumasına olanak tanır.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(1);
// Extract user defined cells of the shape
foreach (User user in shape.Users)
{
    Console.WriteLine(user.Name + ": " + user.Value.Val);
}

{{< /highlight >}}



Bu görüntü, yukarıdaki kodu çalıştırdıktan sonraki çıktıyı gösterir:

![yapılacaklar:resim_alternatif_Metin](working-with-user-defined-cells_2.png)
## **ShapeSheet'te Kullanıcı Tanımlı Hücre Oluşturma**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) şekil sayfasında kullanıcı tanımlı hücre oluşturmaya izin verir. Bu örnek konu, geliştiricilerin ihtiyaç duydukları kadar Kullanıcı.adı satırı ekleyebilecekleri, satırlara anlamlı adlar atayabilecekleri ve hücre değerleri ayarlayabileceklerini açıklamaktadır.
### **Kullanıcı Tanımlı Hücre Oluştur**
Kullanıcılar Koleksiyonu tarafından sunulan Add yöntemi, şekil sayfasında kullanıcı tanımlı bir hücre oluşturmak için kullanılabilir. Tek bir parametre alır.
#### **Hücre Programlama Örneği Oluşturma**
Aspose.Diagram for .NET kullanarak şekil sayfasında kullanıcı tanımlı hücre oluşturmak için .NET uygulamanızda aşağıdaki kod örneğini kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(2);
            
// Initialize user object
User user = new User();
user.Name = "UserDefineCell";
user.Value.Val = "800";
// Add user-defined cell
shape.Users.Add(user);

// Save diagram
diagram.Save(dataDir + "CreateUserDefinedCellInShapeSheet_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Şekil Sayfasından Kullanıcı Tanımlı Hücreleri Al**
Aspose.Diagram for .NET API, şekil sayfasından kullanıcı tanımlı hücrelerin alınmasına izin verir. Bu örnek konu, geliştiricilerin bir çizimdeki tüm şekiller için tüm User.name'yi nasıl alabileceğini açıklamaktadır.
### **Kullanıcı Tanımlı Hücreleri Al**
User sınıfı tarafından sunulan NameU, Value.Val ve Prompt.Value özellikleri, şekil sayfasından kullanıcı tanımlı hücreleri almak için kullanılabilir.
#### **Şekil Sayfası Programlama Örneklerinden Hücreleri Alma**
Aspose.Diagram for .NET'i kullanarak tüm kullanıcı tanımlı hücreleri şekil sayfasından almak için .NET uygulamanızda aşağıdaki kodu kullanın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();
int count = 0;
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through pages
foreach (Aspose.Diagram.Page objPage in diagram.Pages)
{
    // Iterate through shapes
    foreach (Aspose.Diagram.Shape objShape in objPage.Shapes)
    {
        Console.WriteLine(objShape.NameU);
        // Iterate through user-defined cells
        foreach (Aspose.Diagram.User objUserField in objShape.Users)
        {
            count++;
            Console.WriteLine(count + " - Name: " + objUserField.NameU + " Value: " + objUserField.Value.Val + " Prompt: " + objUserField.Prompt.Value);
        }
    }
}  

{{< /highlight >}}

