---
title: Aspose.Diagram for Java 20.5 发行说明
type: docs
weight: 30
url: /zh/java/aspose-diagram-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for Java 20.5 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50487|将 VSD 转换为 SVG 时移位的文本项|强化|
|DIAGRAMJAVA-50692|将 VSDX 另存为 SVG 时粗体文本位置不正确|强化|
|DIAGRAMJAVA-50693|输出 SVG 中不存在图像|漏洞|
|DIAGRAMJAVA-50695|无法将 VSDX 文件另存为图像 - 它会抛出 NullPointerException|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公共 API 所做的任何更改的列表，例如添加、重命名、删除或弃用的成员，以及对 JAVA 对 Aspose.Diagram 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在 Aspose.Diagram 支持论坛上提出。
### **在形状中添加 isIntersect**
指示此形状是否与另一个形状相交。

{{< highlight "java" >}}

 boolean isIntersect = s1.isIntersect(s2);

{{< /highlight >}}
