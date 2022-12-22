---
title: 公共 API Aspose.Diagram 16.11.0 的变化
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-diagram-16-11-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 6.8.0 到 16.11.0 的变化，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **修改 ActiveX 控件的属性**
开发人员可以检索 ActiveX 控件，然后修改其属性。我们在中添加了 ActiveXControl 属性[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)班级。请检查此代码示例：

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"C:\temp\Drawing1.vsd");

// get a Visio page by name

Page page = diagram.Pages.GetPage("Page-1");

// get a shape by ID

Shape shape = page.Shapes.GetShape(1);

// get an ActiveX control

CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;

// set width of the command button control

cbac.Width = 4;

// set height of the command button control

cbac.Height = 4;

// set caption of the command button control

cbac.Caption = "Test Button";

// save diagram

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

呈现宏“代码”时出错：为参数 lang 指定的值无效
## **在 Visio Diagram 中插入一个文本形状**
开发人员可以使用 Aspose.Diagram API 在 Visio diagram 中插入文本形状。请查看此代码示例：

**C#**

{{< highlight "csharp" >}}

 // create a new diagram

Diagram diagram = new Diagram();

// set parameters

double PinX = 1, PinY = 1, Width = 1, Height = 1;

string text = "Test text";

// add text to a Visio page

diagram.Pages[0].AddText(PinX, PinY, Width, Height, text);

// save diagram 

diagram.Save(@"C:\temp\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

呈现宏“代码”时出错：为参数 lang 指定的值无效
