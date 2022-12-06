---
title: Aspose.Diagram for .NET 6.3.0 发行说明
type: docs
weight: 90
url: /zh/net/aspose-diagram-for-net-6-3-0-release-notes/
---
## **其他改进和变化**

|**钥匙** |**概括** |**类别** |
|:- |:- |:- |
|DIAGRAMNET-50739 |添加检测Visio diagram类型的支持。|新功能|
|DIAGRAMNET-50746 |防止导出 PDF 中隐藏的 Visio 页。|新功能|
|DIAGRAMNET-50747 |防止导出 HTML 中隐藏的 Visio 页面。|新功能|
|DIAGRAMNET-50750 |防止导出 PNG 中隐藏的 Visio 页面。|新功能|
|DIAGRAMNET-50751 |防止导出 JPEG 中隐藏的 Visio 页面。|新功能|
|DIAGRAMNET-50752 |防止导出 SVG 中隐藏的 Visio 页面。|新功能|
|DIAGRAMNET-50753 |防止导出 GIF 中隐藏的 Visio 页面。|新功能|
|DIAGRAMNET-50754 |防止导出 XPS 中隐藏的 Visio 页面。|新功能|
|DIAGRAMNET-50541 | VSDX 到 PDF 转换，希伯来语文本项目以相反的顺序呈现。|强化|
|DIAGRAMNET-50542 | VSD转PDF，阿拉伯字转字母。|强化|
|DIAGRAMNET-50682 | VSD 导出为PDF，表格单元格的文字部分不可见。|漏洞|
|DIAGRAMNET-50712 | VDX 到 PDF 导出 - 各种形状的文本错位。|漏洞|
|DIAGRAMNET-50741 | VSD 到 SVG 导出缺少一些 Visio 形状。|漏洞|
|DIAGRAMNET-50742 | VSD 到 SVG 导出未应用形状的内部白色。|漏洞|
|DIAGRAMNET-50744 |VSDX 的打开和保存例程已将文本更改为虚拟字符。|漏洞|
|DIAGRAMNET-50745 | VSDX的打开保存例程改变了虚线整形器。|漏洞|
|DIAGRAMNET-50748 | VSD 到 PDF 导出 - 文本项错放。|漏洞|
|DIAGRAMNET-50763 | VSD 到 VDX 导出抛出主元素错误。|漏洞|
### **公共 API 和向后不兼容的更改**
请参阅列表以了解对公众 API 所做的任何更改，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
#### **添加 FileFormatUtil 和 FileFormatInfo 类**
这些类提供编程访问来检测 Visio 文件类型。
#### **在 FileFormatUtil 类中添加 DetectFileFormat 方法**
它检测并返回有关文件中存储的 Visio diagram 格式的信息。
#### **在 FileFormatInfo 类中添加 FileFormatType 属性**
它获取检测到的文件格式。
#### **在 FileFormatInfo 中添加 LoadFormat 属性**
它获取检测到的加载格式。
#### **在 SVGSaveOptions、XPSSaveOptions、ImageSaveOptions、HTMLSaveOptions 和 PdfSaveOptions 类中添加 ExportHiddenPage 属性**
它定义是否需要导出隐藏的 Visio 页面。
### **使用示例**
请查看 Aspose.Diagram Wiki 文档中添加的帮助主题列表：

- [控制导出隐藏的 Visio 页面保存](/diagram/zh/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
- [检测Visio文件格式](/diagram/zh/net/introduction/#detect-the-format-of-visio-file)
