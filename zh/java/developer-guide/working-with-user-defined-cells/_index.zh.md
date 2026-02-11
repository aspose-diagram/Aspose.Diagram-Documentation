---
title: 使用用户定义的单元格
type: docs
weight: 100
url: /zh/java/working-with-user-defined-cells/
---
## **读取 Visio 形状的用户定义单元格**
用户将文本字段插入到形状中以显示附加信息。**用户定义的单元格**是这些字段的一个分支，该分支使用在形状的 ShapeSheet 中用户定义的单元格部分的值单元格中输入的信息。开发人员可以使用插入和读取所有用户定义的单元格[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

公开的用户集合[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)类支持 com.aspose.diagram.User 对象。这[用户](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)类可用于读取属性。您可以在下图中看到一些用户定义的单元格：

**显示有关用户定义的单元格信息的表格** 

![待办事项：图片_替代_文本](working-with-user-defined-cells_1.png)

以下代码用于读取用户定义的单元格。

下图显示了运行代码后的输出：

![待办事项：图片_替代_文本](working-with-user-defined-cells_2.png)
#### **编程示例**

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

### **创建用户定义的单元格**
Aspose.Diagram for Java API 允许开发人员在形状表中创建用户定义的单元格。此示例主题描述了如何根据需要添加尽可能多的用户名行、为行分配有意义的名称以及设置单元格值。

Users 集合公开的 add 方法可用于在形状表中创建用户定义的单元格。它需要一个参数。

在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 在形状表中创建用户定义的单元格。
#### **编程示例**

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

## **从形状表中检索用户定义的单元格**
Aspose.Diagram for Java API 允许开发人员从形状表中检索用户定义的单元格。此示例主题描述如何检索绘图中所有形状的所有用户名。
### **检索用户定义的单元格**
getNameU()、getValue().getVal() 和 getPrompt().getValue() 方法由[用户](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)类可用于从形状表中检索用户定义的单元格。
#### **从形状表编程示例中检索单元格**
在 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 从形状表中检索所有用户定义的单元格。
#### **编程示例**

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

