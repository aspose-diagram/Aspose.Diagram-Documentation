---
title: 公共 API Aspose.Diagram 6.3.0 的变化
type: docs
weight: 40
url: /zh/java/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 6.0.0 到 6.3.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **检测 Visio 文件的格式**
### **添加各种类、方法和属性以检测格式**
- **添加 FileFormatUtil 和 FileFormatInfo 类** 
 这些类提供程序访问以检测 Visio 文件类型。
- **在 FileFormatUtil 类中添加 detectFileFormat 方法** 
 它检测并返回有关文件中存储的 Visio diagram 格式的信息。
- **在 FileFormatInfo 类中添加 FileFormatType 属性** 
 它获取检测到的文件格式。
- **在 FileFormatInfo 中添加 LoadFormat 属性** 
 它获取检测到的加载格式。

开发人员可以轻松检测任何 Visio 文件的格式。此帮助主题说明了如何检测 Visio 文件格式（使用文件路径或流）并检查其扩展名：[检测Visio文件格式](/diagram/zh/java/introduction/#Introduction-DetecttheFormatofVisioFile)
## **控制导出隐藏的 Visio 页面保存**
### **在 SVGSaveOptions、XPSSaveOptions、ImageSaveOptions、HTMLSaveOptions 和 PdfSaveOptions 类中添加 setExportHiddenPage**
- 它定义是否需要导出隐藏的 Visio 页面。

开发人员可以在将 Visio diagram 保存为 PDF、HTML、图像（PNG、JPEG、GIF）、SVG 和 XPS 文件时包含或排除隐藏的 Visio 页面。此帮助主题说明了如何执行此操作：[控制导出隐藏的 Visio 页面保存](/diagram/zh/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
