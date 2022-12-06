---
title: Aspose.Diagram for Java 16.11.0 发行说明
type: docs
weight: 20
url: /zh/java/aspose-diagram-for-java-16-11-0-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for Java 16.11.0](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-16-11-0-release-notes/).

{{% /alert %}} 
## **其他改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50356|将 VSD 导出为 PDF 时出现性能问题。|强化|
|DIAGRAMJAVA-50419|无法在 VSDM 中设置 ActiveX 按钮的宽度和高度。|强化|
|DIAGRAMJAVA-50257|VSD 到 VDX 的转换，创建了一个无效的结果文件。|漏洞|
|DIAGRAMJAVA-50335|VSDX 到 PDF 导出 - 形状的实线转换为虚线。|漏洞|
|DIAGRAMJAVA-50353|在将 VSD 页面转换为 PNG 时，黑色条带代替了文本。|漏洞|
|DIAGRAMJAVA-50388|将 VSD 页面转换为 PNG 时，右上角文本位置会出现黑色条纹。|漏洞|
|DIAGRAMJAVA-50402|将 Visio 页面转换为 SVG 时，菜单图标无法正确显示。|漏洞|
|DIAGRAMJAVA-50403|在将 Visio 页面转换为 SVG 时，黑色条带出现在表单的文本项的位置。|漏洞|
|DIAGRAMJAVA-50410|在 VSDM 中，形状在分组和保存时变得不可见。|漏洞|
|DIAGRAMJAVA-50413|将 VST 转换为 PDF 时缺少形状。|漏洞|
|DIAGRAMJAVA-50426|将 VSD 转换为 SVG 时不会保留页面的背景颜色。|漏洞|
|DIAGRAMJAVA-50427|打开并保存 VSDX - 十字标志出现在各种形状的地方。|漏洞|
|DIAGRAMJAVA-50428|打开并保存 VSDX - 形状的文本变成虚拟字符。|漏洞|
|DIAGRAMJAVA-50430|无法添加形状菜单项（操作）。|漏洞|
|DIAGRAMJAVA-50431|VSDM 中的连接器未正确连接。|漏洞|
|DIAGRAMJAVA-50432|将 Visio 保存为 PDF 时文本项未对齐。|漏洞|
|DIAGRAMJAVA-50433|将 Visio 保存为 PDF 时，连接线的宽度会发生变化。|漏洞|
### **公共 API 和向后不兼容的更改**
请参阅列表以了解对公众 API 所做的任何更改，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for Java 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Page 类中添加 addText 方法**
它允许添加带有 PinX 和 PinY 值的文本。
### **在 Shape 类中添加 getActiveXControl 方法**
它允许从 Shape 对象获取 ActiveX 控件并设置其属性。
### **使用示例**
请查看 Aspose.Diagram Wiki 文档中添加的帮助主题列表：

1. [在 Visio 页面中插入一个文本形状](/diagram/zh/java/working-with-text/#insert-a-text-shape-in-the-visio-page)
1. [从形状对象中检索 ActiveX 控件以修改属性](/diagram/zh/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/)
