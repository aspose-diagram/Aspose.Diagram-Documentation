---
title: 以编程方式打开 Visio 文档
linktitle: 打开 Visio 文件
type: docs
weight: 20
url: /zh/java/open-visio-document/
description: 本页介绍如何使用 Aspose.Diagram 库从头开始打开 Visio 文档。
---
## **阅读现有的 Visio 图纸**
Aspose.Diagram API 支持从头开始创建新的 Visio 图表，然后以任何支持的文件格式保存。开发者也可以加载现有的 Visio diagram 用于修改、添加或处理目的。
### **读一 Diagram**
使用 Aspose.Diagram API，开发者可以加载所有支持的 Visio 文件格式。 Diagram 类的可用构造函数允许这样做，并且它们接受有效的文件路径字符串或源 Visio 文件的文件流。

支持的可读文件格式如下：
**VSDX, VSD, VSDM, VSS, VSSM, VSSX, VTX, VDX, VDW, VST, VSTX, VSTM and VSX**

diagram 类的构造函数还提供了一个可选参数，用于定义 LoadFileFormat 或 LoadOptions。它是开发者可以传递给 Aspose.Diagram API 的预加载信息。我们建议传递现实信息以获得理想的性能。
#### **阅读 Diagram 编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
