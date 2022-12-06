---
title: Aspose.Diagram Java 对于红宝石
type: docs
weight: 10
url: /zh/java/aspose-diagram-java-for-ruby/
---
## **介绍**
### **Rjb - 红宝石 Java 桥**
RJB 是一个桥接程序，它使用 Java Native Interface 连接 Ruby 和 Java。 Rake + Rjb 是比 Maven 和 Ant 都更强大和有用的构建工具。您可以使用 Rjb 的模拟测试您的 Java 业务逻辑类本身。它有助于将 Struts 的模型对象迁移到您的 RoR 应用程序中。但要注意构建 Swing 应用程序，Ruby（和 Rjb）不考虑 JVM 的本机线程处理。
### **Aspose.Diagram for Java**
Aspose.Diagram for Java是一个非晶格且结构良好的API比 Microsoft Office Automation 提供更好的性能并且更易于使用来操作图表和转换文件。
### **Aspose.Diagram Java 红宝石**
Ruby 项目 Aspose.Diagram Java 展示了如何在 Ruby 中使用 Aspose.Diagram Java API 执行不同的任务。该项目旨在为希望在使用 Rjb（Ruby Java Bridge）的 Ruby 项目中利用 Aspose.Diagram for Java 的 Ruby 开发人员提供有用的示例。
## **系统要求和支持的平台**
### **系统要求**
**以下是对 Ruby 使用 Aspose.Diagram Java 的系统要求：**

- Rjb Gem 已配置
- 下载 Aspose.Diagram 组件
### **支持的平台**
**以下是支持的平台：**

- Ruby 2.2.x 或更高版本以及相应的 DevKit。
- Java 1.5或以上
## **下载**
### **下载所需的库**
下载下面提到的所需库。这些是为 Ruby 示例执行 Aspose.Diagram Java 所必需的。

- [Aspose.Diagram for Java 组件](http://www.aspose.com/community/files/72/java-components/diagram-java/default.aspx)
### **从社交编码网站下载示例**
以下版本的运行示例可在下面提到的社交编码网站上下载：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_Ruby)
## **安装与使用**
### **安装中**
安装 Aspose.Diagram Java for Ruby gem 非常简单易行，请按照说明操作：

运行以下命令。

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
### **使用**
包含将 visio 绘图导出为 Pdf 文档所需的文件。

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

让我们理解上面的代码。

1. 第一行确保 Aspose.Diagram 已加载并可用。
1. 包括访问 Aspose.Diagram 所需的文件
1. 初始化库。 aspose Java 类是从 aspose.yml 文件中提供的路径加载的
## **支持、扩展和贡献**
### **支持**
从 Aspose 成立之初，我们就知道仅仅为客户提供好的产品是不够的。我们还需要提供良好的服务。我们自己也是开发人员，并且了解当技术问题或软件中的怪癖阻止您做您需要做的事情时是多么令人沮丧。我们来这里是为了解决问题，而不是制造问题。

这就是我们提供免费支持的原因。凡是使用过我们产品的人，无论是购买过的还是正在评价中的，都值得我们充分的关注和尊重。

您可以使用以下任何平台记录与 Aspose.Diagram Java for Ruby 相关的任何问题或建议：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/issues)
### **扩展和贡献**
Aspose.Diagram Java for Ruby 是开源的，其源代码可在下面列出的主要社交编码网站上获得。鼓励开发人员下载源代码并通过建议或添加新功能或改进现有功能来做出贡献，以便其他人也可以从中受益。
### **源代码**
您可以从以下位置之一获取最新的源代码：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_Ruby)
## **示例代码示例**
**本节包括以下主题：**

- [在 Ruby 中下载并配置 Aspose.Diagram](/diagram/zh/java/download-and-configure-aspose-diagram-in-ruby/)
- [Ruby 程序员指南](/diagram/zh/java/ruby-programmers-guide/)
  - [在 Ruby 中加载、保存和转换](https://docs.aspose.com/diagram/java/loading-saving-and-converting-in-ruby/)
    - [在 Ruby 中创建一个新的 Visio 绘图](/diagram/zh/java/creating-a-new-visio-drawing-in-ruby/)
    - [Export Visio Diagram to HTML in Ruby](/diagram/zh/java/export-visio-diagram-to-html-in-ruby/)
    - [将 Visio Diagram 导出到 Ruby 中的图像](/diagram/zh/java/export-visio-diagram-to-image-in-ruby/)
    - [Export Visio Diagram to PDF in Ruby](/diagram/zh/java/export-visio-diagram-to-pdf-in-ruby/)
    - [Export Visio Diagram to SVG in Ruby](/diagram/zh/java/export-visio-diagram-to-svg-in-ruby/)
    - [Export Visio Diagram to XAML in Ruby](/diagram/zh/java/export-visio-diagram-to-xaml-in-ruby/)
    - [在 Ruby 中将 Visio Diagram 导出到 XML](/diagram/zh/java/export-visio-diagram-to-xml-in-ruby/)
    - [Export Visio Diagram to XPS in Ruby](/diagram/zh/java/export-visio-diagram-to-xps-in-ruby/)
    - [在 Ruby 中打开现有的 Visio 绘图](/diagram/zh/java/open-an-existing-visio-drawing-in-ruby/)
    - [在 Ruby 中保存 Visio 文档](/diagram/zh/java/saving-visio-document-in-ruby/)
  - [与 Ruby 大师一起工作](/diagram/zh/java/working-with-masters-in-ruby/)
    - [检查 Visio Ruby 绘图中是否存在大师](/diagram/zh/java/check-presence-of-a-master-in-the-visio-drawing-in-ruby/)
    - [从 Ruby 绘图中获取主对象](/diagram/zh/java/get-master-object-from-drawing-in-ruby/)
    - [在 Ruby 中检索大师信息](/diagram/zh/java/retrieve-the-masters-information-in-ruby/)
  - [在 Ruby 中使用图表](/diagram/zh/java/working-with-diagrams-in-ruby/)
    - [在 Ruby 中创建一个空的 Visio Diagram](/diagram/zh/java/create-an-empty-visio-diagram-in-ruby/)
    - [在 Ruby 中检索 Visio 连接器信息](/diagram/zh/java/retrieve-visio-connectors-information-in-ruby/)
    - [在 Ruby 中检索绘图字体信息](/diagram/zh/java/retrieve-drawing-font-information-in-ruby/)
    - [在 Ruby 中为 Visio 绘图添加评论](/diagram/zh/java/add-comments-to-visio-drawings-in-ruby/)
    - [从 Ruby 中的 Visio Diagram 中删除所有宏](/diagram/zh/java/remove-all-macros-from-the-visio-diagram-in-ruby/)
  - [在 Ruby 中使用页面](/diagram/zh/java/working-with-pages-in-ruby/)
    - [从 Ruby 中的 Visio 绘图中获取页面对象](/diagram/zh/java/get-a-page-object-from-visio-drawing-in-ruby/)
    - [在 Ruby 中将新的空白页插入到 Visio 绘图中](/diagram/zh/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/)
    - [在 Ruby 中检索 Visio 页面信息](/diagram/zh/java/retrieve-visio-page-information-in-ruby/)
  - [在 Ruby 中使用形状](/diagram/zh/java/working-with-shapes-in-ruby/)
    - [在 Ruby 中更改形状的位置](/diagram/zh/java/change-the-position-of-a-shape-in-ruby/)
    - [在 Ruby 中连接组的子形状](/diagram/zh/java/connect-sub-shapes-of-the-groups-in-ruby/)
    - [从 Ruby 中的 Visio 页面中提取所有图像](/diagram/zh/java/extract-all-images-from-a-visio-page-in-ruby/)
    - [在 Ruby 中获取各种 Visio 形状的图标](/diagram/zh/java/get-icons-of-various-visio-shapes-in-ruby/)
    - [在 Ruby 中读取 Visio 形状数据](/diagram/zh/java/read-visio-shape-data-in-ruby/)
    - [在Ruby中替换Visio Diagram的图片形状](/diagram/zh/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/)
    - [在 Ruby 中检索 Visio 形状信息](/diagram/zh/java/retrieve-visio-shape-information-in-ruby/)
    - [在 Ruby 中以合适的角度旋转形状](/diagram/zh/java/rotate-a-shape-with-suitable-angle-in-ruby/)
    - [在 Ruby 中选择连接器形状的重新布线选项](/diagram/zh/java/select-reroute-option-of-the-connector-shape-in-ruby/)
    - [在 Ruby 中设置连接器类型形状的外观 Visio](/diagram/zh/java/set-appearance-of-the-connector-type-shape-in-visio-in-ruby/)
    - [在 Ruby 中设置里程碑形状属性](/diagram/zh/java/set-milestone-shape-properties-in-ruby/)
    - [在 Ruby 中设置形状的高度和宽度](/diagram/zh/java/set-the-height-and-width-of-a-shape-in-ruby/)
    - [在 Ruby 中设置 Visio 形状的填充数据](https://docs.aspose.com/diagram/java/set-visio-shape-s-fill-data-in-ruby/)
    - [在 Ruby 中设置 Visio 形状的线数据](https://docs.aspose.com/diagram/java/set-visio-shape-s-line-data-in-ruby/)
    - [在 Ruby 中设置 Visio Shape 的 XForm 数据](https://docs.aspose.com/diagram/java/set-visio-shape-s-xform-data-in-ruby/)
  - [在 Ruby 中使用文本](/diagram/zh/java/working-with-text-in-ruby/)
    - [将自定义样式表应用于 Ruby 中的 Visio Diagram](/diagram/zh/java/apply-custom-style-sheet-to-a-visio-diagram-in-ruby/)
    - [在 Ruby 中对形状的每个文本值应用不同的样式](/diagram/zh/java/apply-different-style-on-the-each-text-value-of-a-shape-in-ruby/)
    - [在 Ruby 中更新 Visio 形状文本](/diagram/zh/java/update-visio-shape-text-in-ruby/)
  - [在 Ruby 中使用窗口元素](/diagram/zh/java/working-with-window-elements-in-ruby/)
    - [在 Ruby 中添加对动态网格和连接点的支持](/diagram/zh/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/)
    - [将窗口元素添加到 Ruby 中的 Visio 实例](/diagram/zh/java/add-window-element-to-the-visio-instance-in-ruby/)
    - [从 Ruby 中的 Visio 绘图中检索窗口元素](/diagram/zh/java/retrieve-window-elements-from-the-visio-drawing-in-ruby/)
    - [在 Ruby 中显示和隐藏 Visio Diagram 的网格、标尺、参考线和分页符](https://docs.aspose.com/diagram/java/show-and-hide-grids-2c-rulers-2c-guides-and-page-breaks-of-the-visio-diagram-in-ruby/)
  - [在 Ruby 中使用 SolutionXML 元素](/diagram/zh/java/working-with-solutionxml-elements-in-ruby/)
    - [将 SolutionXML 元素添加到 Ruby 中的 Visio 绘图](/diagram/zh/java/add-solutionxml-element-to-the-visio-drawing-in-ruby/)
    - [从 Ruby 中的 SolutionXML 元素读取 XML 值](/diagram/zh/java/reading-xml-values-from-the-solutionxml-element-in-ruby/)
  - [在 Ruby 中使用页眉和页脚](/diagram/zh/java/working-with-headers-and-footers-in-ruby/)
    - [在 Ruby 中管理 Visio 图的页眉和页脚](/diagram/zh/java/manage-headers-and-footers-of-the-visio-diagrams-in-ruby/)
  - [在 Ruby 中使用层](/diagram/zh/java/working-with-layers-in-ruby/)
    - [在Ruby Visio Diagram 中添加一个新Layer](/diagram/zh/java/add-a-new-layer-in-the-visio-diagram-in-ruby/)
    - [在 Visio 中用 Ruby 中的图层配置形状对象](/diagram/zh/java/configure-shape-objects-with-layers-in-visio-in-ruby/)
    - [从 Ruby 中的 Visio Diagram 中检索所有图层](/diagram/zh/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/)
  - [在 Ruby 中使用超链接](/diagram/zh/java/working-with-hyperlinks-in-ruby/)
    - [在 Ruby 中将超链接添加到 Visio 形状](/diagram/zh/java/add-hyperlink-to-a-visio-shape-in-ruby/)
    - [从 Ruby 中的 Visio 绘图中获取形状超链接数据](/diagram/zh/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/)
  - [在 Ruby 中使用用户定义的单元格](/diagram/zh/java/working-with-user-defined-cells-in-ruby/)
    - [在 Ruby 的 ShapeSheet 中创建用户定义的单元格](/diagram/zh/java/create-user-defined-cell-in-the-shapesheet-in-ruby/)
    - [在 Ruby 中读取 Shape 的用户定义单元格](https://docs.aspose.com/diagram/java/read-shape-s-user-defined-cells-in-ruby/)
    - [在 Ruby 中从形状表中检索用户定义的单元格](/diagram/zh/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/)
  - [在 Ruby 中使用保护](/diagram/zh/java/working-with-protection-in-ruby/)
    - [在 Ruby 中保护和取消保护 Visio 形状](/diagram/zh/java/protect-and-unprotect-a-visio-shape-in-ruby/)
    - [在 Ruby 中保护和取消保护图](/diagram/zh/java/protect-and-unprotect-diagrams-in-ruby/)
  - [在 Ruby 中使用几何部分](/diagram/zh/java/working-with-geometry-section-in-ruby/)
    - [在 Ruby 中编辑 ShapeSheet 中的连接器几何部分](/diagram/zh/java/edit-connector-geometry-section-in-the-shapesheet-in-ruby/)
- [在 Ruby 中支持、扩展和贡献 Aspose.Diagram](https://docs.aspose.com/diagram/java/support-extend-and-contribute-to-aspose-diagram-in-ruby/)
