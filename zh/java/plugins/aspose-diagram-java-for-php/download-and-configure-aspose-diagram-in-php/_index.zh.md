---
title: 在 PHP 中下载并配置 Aspose.Diagram
type: docs
weight: 10
url: /zh/java/download-and-configure-aspose-diagram-in-php/
---
## **下载所需的库**
下载下面提到的所需库。这些是为 Ruby 示例执行 Aspose.Diagram Java 所必需的。

- [Aspose.Diagram for Java 组件](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **从社交编码网站下载示例**
以下版本的运行示例可在下面提到的社交编码网站上下载：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **安装中**
安装 Aspose.Diagram Java for PHP 非常简单易行，请按照说明操作：

运行以下命令。

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **使用**
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
