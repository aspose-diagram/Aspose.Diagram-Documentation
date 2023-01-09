---
title: 在 Ruby 中保存 Visio 文档
type: docs
weight: 100
url: /zh/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - 保存 Visio 文件**
保存 Visio 文档使用**Aspose.Diagram Java 红宝石**，您可以使用以下代码。

**红宝石代码**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
