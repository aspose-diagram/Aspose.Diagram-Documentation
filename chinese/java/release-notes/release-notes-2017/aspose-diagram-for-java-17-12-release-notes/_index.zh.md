---
title: Aspose.Diagram for Java 17.12 发行说明
type: docs
weight: 10
url: /zh/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|提供单个 API 将 Visio 形状转换为 PDF|强化|
|DIAGRAMJAVA-50291|提供单个 API 将 Visio 形状转换为 HTML|强化|
|DIAGRAMJAVA-50572|Shape.connectedShapes 方法不检索传出节点|强化|
|DIAGRAMJAVA-50391|翻转的图像和箭头是在将 VSD 转换为 SVG 时生成的|漏洞|
|DIAGRAMJAVA-50570|VSD 到 PDF - 添加了额外的文本项|漏洞|
|DIAGRAMJAVA-50571|导入 VSDX - 形状元素发生错误|漏洞|
|DIAGRAMJAVA-50573|VSD 到 SVG - 缺少组形状的线条|漏洞|
|DIAGRAMJAVA-50575|VSD 到 SVG - 缺少文本项|漏洞|
|DIAGRAMJAVA-50576|导入 VDX 过程抛出页面元素错误|漏洞|
### **在 Shape 类中添加 Copy 成员**
复制成员采用目标形状实例作为参数来克隆此形状。

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **在 Shape 类中添加 toPdf 成员**
toPdf 成员将形状转换为 PDF 格式。

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **在 Shape 类中添加 toHTML 成员**
toHTML 成员将形状转换为 PDF 格式。

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **使用示例**
请查看 Aspose.Diagram Wiki 文档中添加的帮助主题列表：

1. [将 Visio Shape 复制到另一个 Shape 实例](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [将 Visio 形状转换为 PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [将 Visio 形状转换为 HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


