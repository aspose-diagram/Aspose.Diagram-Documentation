---
title: Aspose.Diagram 为 Python 通过 Java 22.6 发行说明
type: docs
weight: 22
url: /zh/java/aspose-diagram-for-python-via-java-22-6-release-notes/
---
{{% alert color="primary" %}}

此页面包含 Aspose.Diagram 的发行说明信息，适用于 Python via Java 22.6。

{{% /alert %}}
## **改进和变化**  ##

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMJAVA-50963|WK：保存为 PNG 后形状变形|强化|
|DIAGRAMJAVA-50967|调整侧线形状 [续]|漏洞|
|DIAGRAMJAVA-50972|API 没有正确解析文件|漏洞|
|DIAGRAMJAVA-50974|添加新连接点的问题|漏洞|

## `?`**公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for Java 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。

### **在 HTMLSaveOptions 中添加分辨率**
- 获取或设置生成的 html 的分辨率，以每英寸点数为单位

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.setResolution(96);
{{< /highlight >}}
