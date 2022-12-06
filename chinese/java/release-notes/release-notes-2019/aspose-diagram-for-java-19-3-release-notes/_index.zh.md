---
title: Aspose.Diagram for Java 19.3 发行说明
type: docs
weight: 100
url: /zh/java/aspose-diagram-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for Java 19.3 的发行说明

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50339|添加对在操作系统上检索常用字体目录的支持|强化|
|DIAGRAMJAVA-50097|VSD 到PDF转换-曲线变成直线|漏洞|
|DIAGRAMJAVA-50161|VTX 到 HTML 转换 - 整个 diagram 的背景图片丢失|漏洞|
|DIAGRAMJAVA-50301|VSD 到 PDF 导出 - 元类型形状变成混乱的符号|漏洞|
|DIAGRAMJAVA-50464|将 VSDX 转换为 PNG 时形状呈现不正确|漏洞|
|DIAGRAMJAVA-50652|VISIO 到 PDF - 输出 PDF 在 Adobe Reader 中显示错误|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for Java 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Diagram 中添加 GetDefaultFontDir**
获取默认字体文件夹路径

{{< highlight "java" >}}

  string str =  diagram.getDefaultFontDir();

{{< /highlight >}}
