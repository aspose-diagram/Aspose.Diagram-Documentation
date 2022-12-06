---
title: Aspose.Diagram 用于 Node.js 通过 Java 21.11 发行说明
type: docs
weight: 4
url: /zh/java/aspose-diagram-for-node-js-via-java-21-11-release-notes/
---
{{% alert color="primary" %}}

此页面包含 Aspose.Diagram for Node.js 的发行说明信息，发布时间为 Java 21.11。

{{% /alert %}}
## **改进和变化**  ##

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50806|wk: InheridetChar 颜色|强化|
|DIAGRAMJAVA-50385|将 VSDX 转换为 PDF 时，边框和标题的颜色会发生变化|漏洞|
|DIAGRAMJAVA-50501|VSDX 到 PNG - 形状颜色不正确|漏洞|
|DIAGRAMJAVA-50631|VSDX 导出为PDF后形状不一致|漏洞|
|DIAGRAMJAVA-50804|绘制连接器时连接器文本换行|漏洞|
## `?`**公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for Java 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。

### **在形状中添加预设主题**
- 将预设主题应用于此形状。

{{< highlight "java" >}}
 
 shape.setPresetTheme( PresetThemeValue.BUBBLE);

{{< /highlight >}}


### **在形状中添加 PresetThemeVariant**
- 将预设主题变体应用于此形状

{{< highlight "java" >}}

shape.setPresetThemeVariant( PresetThemeVariantValue.VARIANT_1);

{{< /highlight >}}

### **在形状中添加 PresetThemeQuickStyle**
- 将预设主题变体 quickstyle 应用于此形状

{{< highlight "java" >}}

shape.setPresetThemeQuickStyle(PresetQuickStyleValue.VARIANT_STYLE_1);

{{< /highlight >}}
