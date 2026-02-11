---
title: 使用页眉和页脚
type: docs
weight: 150
url: /zh/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java 提供了设置 Microsoft Office Visio 图表的页眉和页脚的机制。开发人员可以获取或设置出现在文档页眉/页脚左侧、中间和右侧的文本字符串。他们还可以设置页眉和页脚边距以及文本的字体属性。

{{% /alert %}} 
### **设置页眉和页脚属性**
这[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类对象提供 HeaderFooter 属性，允许获取和设置页眉和页脚文本、字体和边距值。 Visio图纸打印预览时，用户可以点击Microsoft Visio 2013中的“编辑页眉页脚”链接按钮（Microsoft Visio 2010>>“页眉页脚”按钮）。有几个选项可以添加文本，如下面的屏幕截图所示。用户可以使用 Aspose.Diagram API 以编程方式管理这些属性，如下所示：

**管理页眉和页脚文本、边距和字体属性。** 

![待办事项：图片_替代_文本](working-with-headers-and-footers_1.png)

以下代码有助于管理页眉和页脚属性。
#### **编程示例**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
