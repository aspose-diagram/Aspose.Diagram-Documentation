---
title: 使用图层
type: docs
weight: 130
url: /zh/net/working-with-layers/
description: 本节介绍如何使用 Aspose.Diagram 在 visio 形状中添加或获取图层信息。
---
## **在 Visio 中使用图层配置形状对象**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)允许在 Microsoft Office Visio diagram 中配置具有图层的形状对象。每个形状可以属于多个图层，因此开发人员可以管理形状以满足最终用户的需求。这[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类对象提供 LayerMember 属性，允许在 Visio 绘图的图层中添加和删除形状对象。用户可以使用 Aspose.Diagram API 以编程方式管理这些属性，如下所示：
### **配置形状对象编程示例**
以下代码有助于添加、删除和移动形状对象属性。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name.ToLower() == "shape1")
    {
        // Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0;1";
    }
    else if (shape.Name.ToLower() == "shape2")
    {
        // Remove shape2 from all the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "";
    }
    else if (shape.Name.ToLower() == "shape3")
    {
        // Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0";
    }
}
// Save diagram
diagram.Save(dataDir + "ConfigureShapeLayers_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **在Visio Diagram 中添加一个新Layer**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)允许开发人员添加新层来组织形状的自定义类别，然后以编程方式将形状分配给这些层。这[图层集合](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection)类提供 Add 方法，允许添加一个新的[层](http://www.aspose.com/api/net/diagram/aspose.diagram/layer)在 Visio 图纸中。开发者可以通过初始化它的类对象来设置 Layer 的属性。
### **添加层编程示例**
下面的一段代码有助于添加 Layer 对象。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object
Layer layer = new Layer();
// Set Layer name
layer.Name.Value = "Layer1";
// Set Layer Visibility
layer.Visible.Value = BOOL.True;
// Set the color checkbox of Layer
layer.IsColorChecked = BOOL.True;
// Add Layer to the particular page sheet
page.PageSheet.Layers.Add(layer);

// Get shape by ID
Shape shape = page.Shapes.GetShape(3);
// Assign shape to this new Layer
shape.LayerMem.LayerMember.Value = layer.IX.ToString();
// Save diagram
diagram.Save(dataDir + "AddLayer_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **从 Visio Diagram 中检索所有图层**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)允许开发人员获取 Visio diagram 的现有层。[页表](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet)的财产[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类允许使用 Visio diagram 检索可用层的列表[图层集合](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection)班级。
### **检索层编程示例**
以下代码有助于获取图层列表。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Layer layer in page.PageSheet.Layers)
{
    Console.WriteLine("Name: " + layer.Name.Value);
    Console.WriteLine("Visibility: " + layer.Visible.Value);
    Console.WriteLine("Status: " + layer.Status.Value);
}

{{< /highlight >}}
```
