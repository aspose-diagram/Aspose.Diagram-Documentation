---
title: Aspose.Diagram for Java 21.3 发行说明
type: docs
weight: 10
url: /zh/java/aspose-diagram-for-java-21-3-release-notes/
---
{{% alert color="primary" %}}

此页面包含 Aspose.Diagram for Java 21.3 的发行说明信息。

{{% /alert %}}
## **改进和变化**  ##

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50711|尝试将 VDX 文档另存为 PNG 时抛出 NullPointerException|强化|
|DIAGRAMJAVA-50713|将 VSDX 转换为 PDF 时出现文本重叠问题|强化|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for Java 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。
### **在页面中添加 ConnectShapesViaConnector**
- 通过连接器连接形状。

{{< highlight "java" >}}

page.connectShapesViaConnector(id, "Port7", id, "Port21", id);

{{< /highlight >}}
### **在页面中添加 GlueShapeToConnectorBeginX**
- 使用 BeginX 粘贴形状



{{< highlight "java" >}}

page.glueShapeToConnectorBeginX(id, "Port7", id);

{{< /highlight >}}
### **在页面中添加 GlueShapeToConnectorEndX**
- 使用 BeginX 粘贴形状



{{< highlight "java" >}}

page.glueShapeToConnectorEndX(id, "Port21", id);

{{< /highlight >}}
### **在页面中添加 CenterDrawing**
- 使页面的形状相对于页面的范围居中。



{{< highlight "java" >}}

page.centerDrawing();

{{< /highlight >}}
### **在形状中添加 IsContain**
- 指示此形状是否包含另一个形状。



{{< highlight "java" >}}

OLE_Shape.isContain(shape)

{{< /highlight >}}