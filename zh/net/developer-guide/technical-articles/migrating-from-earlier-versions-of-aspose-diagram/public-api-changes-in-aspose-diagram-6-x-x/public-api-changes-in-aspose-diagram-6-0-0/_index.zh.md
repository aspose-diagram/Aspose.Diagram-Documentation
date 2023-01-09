---
title: 公共 API Aspose.Diagram 6.0.0 的变化
type: docs
weight: 40
url: /zh/net/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 5.9.0 到 6.0.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **IsGlued 方法在 Shape 类中添加**
IsGlued 方法将形状对象作为参数来确定两个形状是否粘合。
示例代码：

**C#**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsGlued(ShapedTwo);

{{< /highlight >}}

**虚拟机**

{{< highlight "java" >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsGlued(ShapedTwo)

{{< /highlight >}}
## **Shape 类中添加 IsConnected 方法**
IsConnected 方法将形状对象作为参数来确定两个形状是否连接。
示例代码：

**C#**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.Shapes.GetShape(1);

Shape ShapedTwo = page.Shapes.GetShape(2);

// determine whether shapes are glued

bool glued = ShapedOne.IsConnected(ShapedTwo);

{{< /highlight >}}

**虚拟机**

{{< highlight "java" >}}

 ' Call the diagram constructor to load diagram

Dim diagram As New Diagram("C:/temp/Drawing1.vsdx")

' get Visio page by name

Dim page As Page = diagram.Pages.GetPage("Page-1")

' get Visio shapes by ids

Dim ShapedOne As Shape = page.Shapes.GetShape(1)

Dim ShapedTwo As Shape = page.Shapes.GetShape(2)

' determine whether shapes are glued

Dim glued As Boolean = ShapedOne.IsConnected(ShapedTwo)

{{< /highlight >}}
