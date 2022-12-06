---
title: Aspose.Diagram for Java 17.10 发行说明
type: docs
weight: 30
url: /zh/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JpegQuality 对输出文档没有任何影响|强化|
|DIAGRAMJAVA-50548|输出 VSDX - 穿过形状边界的连接线|漏洞|
|DIAGRAMJAVA-50550|形状变换部分不保留公式|漏洞|
|DIAGRAMJAVA-50551|VSDX 到 PNG - 形状角的渲染不正确|漏洞|
|DIAGRAMJAVA-50552|将 Visio 绘图保存为 SVG 时不会保留填充颜色|漏洞|
|DIAGRAMJAVA-50553|将 Visio 绘图保存为 SVG 时线条渲染不正确|漏洞|
|DIAGRAMJAVA-50554|将 Visio 绘图保存为 SVG 时不会保留填充颜色|漏洞|
|DIAGRAMJAVA-50555|将 Visio 绘图保存为 SVG 时线条渲染不正确|漏洞|
|DIAGRAMJAVA-50559|VSDM 到 VDX - 连接线没有连接到形状|漏洞|
|DIAGRAMJAVA-50561|VSDX 添加 SolutionXML 元素后绘图损坏|漏洞|
### **在 ImageSaveOptions 中添加 SameAsPdfConversionArea**
指定是否像PDF一样保存区域。

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
