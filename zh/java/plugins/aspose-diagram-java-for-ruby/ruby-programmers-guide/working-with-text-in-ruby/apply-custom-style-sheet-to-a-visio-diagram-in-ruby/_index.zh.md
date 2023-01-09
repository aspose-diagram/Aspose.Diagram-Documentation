---
title: 将自定义样式表应用于 Ruby 中的 Visio Diagram
type: docs
weight: 10
url: /zh/java/apply-custom-style-sheet-to-a-visio-diagram-in-ruby/
---
## **Aspose.Diagram - 将自定义样式表应用于 Visio Diagram**
将自定义样式表应用到 Visio Diagram 使用**Aspose.Diagram Java 红宝石** 只需调用**应用自定义样式表**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\# 创建 Diagram 实例

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

形状 = diagram.getPages().getPage(0).getShapes()

我 = 0

当我< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        source_shape = shape

        break

    end

    i +=1

end

\# Find the required style sheet

stylesheets = diagram.getStyleSheets()

j = 0

while j < stylesheets.getCount()

    stylesheet = stylesheets.get(j)

    if stylesheet.getName() == "Basic"

        custom_stylesheet = stylesheet

        break

    end

    j +=1

end

if source_shape != nil && custom_stylesheet != nil

    # Apply text style

    source_shape.setTextStyle(custom_stylesheet)

    # Apply fill style

    source_shape.setFillStyle(custom_stylesheet)

    # Apply line style

    source_shape.setLineStyle(custom_stylesheet)

end

\# Save diagram

diagram.save(data_dir + "ApplyCustomStyleSheet.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied custom stylesheet to a visio diagram."

{{< /highlight >}}
## **下载运行代码**
下载**将自定义样式表应用于 Visio Diagram (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/applycustomstylesheet.rb)
