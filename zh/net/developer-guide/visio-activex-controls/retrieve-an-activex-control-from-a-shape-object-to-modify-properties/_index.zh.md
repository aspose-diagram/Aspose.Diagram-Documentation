---
title: 从形状对象中检索 ActiveX 控件以修改属性
type: docs
weight: 20
url: /zh/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: 使用 Aspose.Diagram 库修改 activeX 控件的属性。
---
{{% alert color="primary" %}} 

使用 Aspose.Diagram API，开发人员可以从 Visio 形状对象中检索 ActiveX 控件以设置其所有可用属性。

{{% /alert %}} 
## **检索 ActiveX 控件编程示例**
[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类提供 ActiveXControl 属性，允许开发人员从 Visio 形状对象检索 ActiveX 控件。开发人员可以在适当的 ActiveX 控件类中转换一个 ActiveX 控件，然后设置它的所有可用属性。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Load and get a Visio page by name
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");            
Page page = diagram.Pages.GetPage("Page-1");
// Get a shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;
// Set width, height and caption of the command button control
cbac.Width = 4;           
cbac.Height = 4;           
cbac.Caption = "Test Button";
// Save diagram
diagram.Save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

