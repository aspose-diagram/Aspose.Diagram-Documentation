---
title: Arbeta med användardefinierade celler
type: docs
weight: 100
url: /sv/java/working-with-user-defined-cells/
---
## **Läs användardefinierade celler i Visio-formerna**
 Användare infogar textfält i former för att visa ytterligare information.**Användardefinierade celler** är den ena grenen av dessa fält och den här grenen använder information som anges i värdecellen i avsnittet Användardefinierade celler i formens ShapeSheet. Utvecklare kan infoga och läsa alla användardefinierade celler med hjälp av[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 Användarsamlingen exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) klass stöder objektet com.aspose.diagram.User. De[Användare](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) klass kan användas för att läsa egenskaper. Det finns några användardefinierade celler som du kan se i följande bild:

**Tabell som visar information om användardefinierade celler** 

![todo:image_alt_text](working-with-user-defined-cells_1.png)

Följande kod används för att läsa användardefinierade celler.

Följande bild visar utdata efter att ha kört koden:

![todo:image_alt_text](working-with-user-defined-cells_2.png)
#### **Programmeringsexempel**

{{< highlight java >}}
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

### **Skapa användardefinierad cell**
Aspose.Diagram for Java API tillåter utvecklare att skapa användardefinierade celler i formarket. Det här exemplet beskriver hur du lägger till så många användarnamnsrader som behövs, tilldelar meningsfulla namn till raderna och ställer in cellvärden.

Add-metoden som exponeras av Users-samlingen kan användas för att skapa användardefinierade celler i formarket. Det krävs en enda parameter.

Använd följande kod i din Java-applikation för att skapa användardefinierad cell i formarket med Aspose.Diagram for Java.
#### **Programmeringsexempel**

{{< highlight java >}}
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

## **Hämta användardefinierade celler från Shapesheet**
Aspose.Diagram for Java API tillåter utvecklare att hämta användardefinierade celler från formark. Det här exemplet beskriver hur man hämtar alla användarnamn för alla former i en ritning.
### **Hämta användardefinierade celler**
 Metoderna getNameU(), getValue().getVal() och getPrompt().getValue() exponerade av[Användare](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)klass kan användas för att hämta användardefinierade celler från formblad.
#### **Hämta celler från Shapesheet-programmeringsexempel**
Använd följande kod i din Java-applikation för att hämta alla användardefinierade celler från formblad med Aspose.Diagram for Java.
#### **Programmeringsexempel**

{{< highlight java >}}
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

