---
title: 以编程方式打开 Visio 文档
linktitle: 打开 Visio 文件
type: docs
weight: 20
url: /zh/net/open-visio-document/
description: 本页介绍如何使用 Aspose.Diagram 库从头开始打开 Visio 文档。
---
## **阅读现有的 Visio 图纸**
Aspose.Diagram API 支持从头开始创建新的 Visio 图表，然后以任何支持的文件格式保存。开发者也可以加载现有的 Visio diagram 用于修改、添加或处理目的。
## **读一 Diagram**
使用 Aspose.Diagram API，开发者可以加载所有支持的 Visio 文件格式。 Diagram 类的可用构造函数允许这样做，并且它们接受有效的文件路径字符串或源 Visio 文件的文件流。

支持的可读文件格式如下：
**VSDX, VSD, VSDM, VSS, VSSX, VSSM, VTX, VSTM, VDX, VDW, VST, VSTX and VSX**

diagram 类的构造函数还提供了一个可选参数，用于定义 LoadFileFormat 或 LoadOptions。它是开发者可以传递给 Aspose.Diagram API 的预加载信息。我们建议传递现实信息以获得理想的性能。
## **阅读 Diagram 编程示例**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD stream
FileStream st = new FileStream(dataDir + "Drawing1.vsdx", FileMode.Open);
Diagram vsdDiagram = new Diagram(st);
st.Close();

// Call the diagram constructor to load a VDX diagram
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load a VSS stencil
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}

