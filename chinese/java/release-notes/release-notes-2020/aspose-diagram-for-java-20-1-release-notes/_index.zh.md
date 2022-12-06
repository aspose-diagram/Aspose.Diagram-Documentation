---
title: Aspose.Diagram for Java 20.1 发行说明
type: docs
weight: 70
url: /zh/java/aspose-diagram-for-java-20-1-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for Java 20.1 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50664|导出到 SVG 时不支持渐变填充|强化|
|DIAGRAMJAVA-50670|允许从内存中加载字体|强化|
|DIAGRAMJAVA-50681|API 加载 diagram 大文件需要很长时间|强化|
|DIAGRAMJAVA-50381|将 VSDX 转换为 PDF 时未保留网络形状|漏洞|
|DIAGRAMJAVA-50386|将 VSD 转换为 SVG 时，图像上下颠倒且存在色差|漏洞|
|DIAGRAMJAVA-50679|VSDX 到 PDF - 输出中缺少连接器|漏洞|
|DIAGRAMJAVA-50680|Visio 到 PNG - 输出图像被裁剪掉|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公共 API 所做的任何更改的列表，例如添加、重命名、删除或弃用的成员，以及对 JAVA 对 Aspose.Diagram 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在 Aspose.Diagram 支持论坛上提出。

- 在 Page 中添加了 getPages 和 setPages - 指定要加载的页面的索引。

{{< highlight "java" >}}

 LoadOptions options = new LoadOptions(LoadFileFormat.VSDX);

options.setPages(new ArrayList());

options.getPages().add(0);

{{< /highlight >}}

- 在 FontConfigs 中添加 setFontSources - 设置字体源。

{{< highlight "java" >}}

 byte[]b = new byte[]{ 0 };

com.aspose.diagram.MemoryFontSource sc1 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource sc2 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource[]sc = new com.aspose.diagram.MemoryFontSource[]{ sc1, sc2 };

com.aspose.diagram.FontConfigs.setFontSources(sc); 

{{< /highlight >}}


