---
title: Insert an ActiveX Control in the Visio Diagram
type: docs
weight: 10
url: /zh/net/insert-an-activex-control-in-the-visio-diagram/
description: 本页介绍如何使用 Aspose.Diagram 库插入 activeX 控件。
---
{{% alert color="primary" %}}

开发者可以直接在Microsoft Visio 绘图中添加ActiveX控件，使Visio diagram 交互使用[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **插入 ActiveX 控件编程示例**
[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类提供 AddActiveXControl 方法并允许开发人员插入任何类型的 ActiveX 控件，如命令按钮、组合框、复选框、列表框、文本框、旋转按钮、单选按钮、标签、图像、切换按钮和滚动条。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// Save diagram
diagram.Save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

