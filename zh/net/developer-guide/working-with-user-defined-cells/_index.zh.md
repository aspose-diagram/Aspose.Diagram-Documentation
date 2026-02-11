---
title: 使用用户定义的单元格
type: docs
weight: 150
url: /zh/net/working-with-user-defined-cells/
description: 本节介绍如何使用 Aspose.Diagram 读取 visio 形状的用户定义单元格。
---
## **读取 Visio 形状的用户定义单元格**
用户将文本字段插入到形状中以显示附加信息。**用户定义的单元格**是这些字段的一个分支，该分支使用在形状的 ShapeSheet 中用户定义的单元格部分的值单元格中输入的信息。开发人员可以使用插入和读取所有用户定义的单元格[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **检索用户定义的单元格字段**
公开的用户集合[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类支持 Aspose.Diagram.User 对象。此属性可用于读取 Visio 形状的用户定义单元格，如形状的 ShapeSheet 的用户定义单元格部分中可用。

![待办事项：图片_替代_文本](working-with-user-defined-cells_1.png)
#### **检索单元格编程示例**
以下代码允许开发人员读取用户定义的单元格字段。


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



此图显示了运行上述代码后的输出：

![待办事项：图片_替代_文本](working-with-user-defined-cells_2.png)
## **在 ShapeSheet 中创建用户定义的单元格**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)允许在形状表中创建用户定义的单元格。此示例主题描述了开发人员可以根据需要添加任意数量的 User.name 行、为行分配有意义的名称以及设置单元格值的方式。
### **创建用户定义的单元格**
用户集合公开的 Add 方法可用于在形状表中创建用户定义的单元格。它需要一个参数。
#### **创建单元格编程示例**
在 .NET 应用程序中使用以下代码示例，使用 Aspose.Diagram for .NET 在形状表中创建用户定义的单元格。


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

## **从形状表中检索用户定义的单元格**
Aspose.Diagram for .NET API 允许从形状表中检索用户定义的单元格。此示例主题描述了开发人员可以检索绘图中所有形状的所有 User.name 的方式。
### **检索用户定义的单元格**
User 类公开的 NameU、Value.Val 和 Prompt.Value 属性可用于从形状表中检索用户定义的单元格。
#### **从形状表编程示例中检索单元格**
在 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 从形状表中检索所有用户定义的单元格。


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

