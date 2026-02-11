---
title: Kullanıcı Tanımlı Hücrelerle Çalışma
type: docs
weight: 100
url: /tr/java/working-with-user-defined-cells/
---
## **Visio Şekillerinin Kullanıcı Tanımlı Hücrelerini Oku**
 Kullanıcılar, ek bilgileri görüntülemek için şekillere metin alanları ekler.**Kullanıcı Tanımlı Hücreler** bu alanların tek dalıdır ve bu dal, şeklin ShapeSheet'indeki Kullanıcı Tanımlı Hücreler bölümünün Değer hücresine girilen bilgileri kullanır. Geliştiriciler, kullanarak tüm kullanıcı tanımlı hücreleri ekleyebilir ve okuyabilir[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 Tarafından sunulan Kullanıcılar koleksiyonu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) sınıf, com.aspose.diagram.User nesnesini destekler. bu[kullanıcı](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) sınıf, özellikleri okumak için kullanılabilir. Aşağıdaki resimde görebileceğiniz gibi, kullanıcı tanımlı birkaç hücre vardır:

**Kullanıcı tanımlı hücreler hakkında bilgileri gösteren tablo** 

![yapılacaklar:resim_alternatif_Metin](working-with-user-defined-cells_1.png)

Aşağıdaki kod, kullanıcı tanımlı hücreleri okumak için kullanılır.

Aşağıdaki görüntü, kodu çalıştırdıktan sonraki çıktıyı gösterir:

![yapılacaklar:resim_alternatif_Metin](working-with-user-defined-cells_2.png)
#### **Programlama Örnekleri**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadUserdefinedCellsOfShape.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(1);
// extract user defined cells of the shape
for (User user :(Iterable<User>) shape.getUsers())
{
    System.out.println(user.getName() + ": " + user.getValue().getVal());
}

{{< /highlight >}}
```
### **Kullanıcı Tanımlı Hücre Oluştur**
Aspose.Diagram for Java API, geliştiricilerin şekil sayfasında kullanıcı tanımlı hücre oluşturmasına olanak tanır. Bu örnek konu, gerektiği kadar çok kullanıcı adı satırının nasıl ekleneceğini, satırlara anlamlı adların nasıl atanacağını ve hücre değerlerinin nasıl ayarlanacağını açıklar.

Kullanıcılar koleksiyonu tarafından sunulan ekleme yöntemi, şekil sayfasında kullanıcı tanımlı hücre oluşturmak için kullanılabilir. Tek bir parametre alır.

Aspose.Diagram for Java kullanarak şekil sayfasında kullanıcı tanımlı hücre oluşturmak için Java uygulamanızda aşağıdaki kodu kullanın.
#### **Programlama Örnekleri**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Şekil Sayfasından Kullanıcı Tanımlı Hücreleri Al**
Aspose.Diagram for Java API, geliştiricilerin şekil sayfasından kullanıcı tanımlı hücreleri almasına olanak tanır. Bu örnek konu, bir çizimdeki tüm şekiller için tüm kullanıcı adlarının nasıl alınacağını açıklar.
### **Kullanıcı Tanımlı Hücreleri Al**
 tarafından sunulan getNameU(), getValue().getVal() ve getPrompt().getValue() yöntemleri[kullanıcı](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)class, kullanıcı tanımlı hücreleri şekil sayfasından almak için kullanılabilir.
#### **Şekil Sayfası Programlama Örneklerinden Hücreleri Alma**
Aspose.Diagram for Java'i kullanarak tüm kullanıcı tanımlı hücreleri şekil sayfasından almak için Java uygulamanızda aşağıdaki kodu kullanın.
#### **Programlama Örnekleri**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
