---
title: 在 Ruby 中打开现有的 Visio 绘图
type: docs
weight: 90
url: /zh/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - 打开现有的 Visio 绘图**
要使用打开现有的 Visio 绘图**Aspose.Diagram Java 红宝石**，您可以使用以下代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
