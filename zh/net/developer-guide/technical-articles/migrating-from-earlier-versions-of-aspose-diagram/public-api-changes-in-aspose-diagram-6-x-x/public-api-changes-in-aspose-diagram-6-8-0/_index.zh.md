---
title: 公共 API Aspose.Diagram 6.8.0 的变化
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 6.6.0 到 6.8.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **插入 ActiveX 控件**
开发者可以在Visio diagram插入一个ActiveX控件，我们在[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)班级。请检查此代码示例：

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

呈现宏“代码”时出错：为参数 lang 指定的值无效
## **设置图层的颜色复选框**
开发者可以使用 Aspose.Diagram API 来设置或获取Layer的Color CheckBox，请查看此代码示例：

**C#**

{{< highlight "csharp" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// Get Visio page

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// Set Layer name

layer.Name.Value = "Layer1";

// Set Layer Visibility

layer.Visible.Value = BOOL.True;

// set the color checkbox of Layer

layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet

page.PageSheet.Layers.Add(layer);

// Get shape by ID

Shape shape = page.Shapes.GetShape(3);

// Assign shape to this new Layer

shape.LayerMem.LayerMember.Value = layer.IX.ToString();

// Save diagram

diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

呈现宏“代码”时出错：为参数 lang 指定的值无效
## **在 Shape 类中添加 InheritFill 属性**
开发人员可以获取或设置继承填充属性。我们在 Shape 类中添加了 InheritFill 属性。请检查此代码示例：

**C#**

{{< highlight "csharp" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID

Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Shape shape = page.Shapes.GetShape(1);

// get the fill formatting values

Console.WriteLine(shape.InheritFill.FillBkgnd.Value);

Console.WriteLine(shape.InheritFill.FillForegnd.Value);

Console.WriteLine(shape.InheritFill.FillPattern.Value);

{{< /highlight >}}

呈现宏“代码”时出错：为参数 lang 指定的值无效
