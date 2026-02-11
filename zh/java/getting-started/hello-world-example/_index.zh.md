---
title: Hello World 示例
type: docs
weight: 100
url: /zh/java/hello-world-example/
---
## **Hello World 示例**
A "Hello World" example is traditionally used to introduce features of a programming language or software with a simple use case.

Aspose.Diagram for Java is a feature-rich Visio file processing API that allows application developers to embed Visio document creation, reading & conversion features in their Java applications. It supports working with many popular Visio file-formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. The API has strong conversion features to convert Visio Diagrams to a number of formats such as PDF, HTML, XML, SVG, and XAML.

后[安装 Aspose.Diagram for Java](/diagram/zh/java/installation/)在您的环境中，您可以执行以下代码示例以查看 Aspose.Diagram API 的工作原理。

下面的代码片段遵循以下步骤：

1. 实例化一个 Diagram 对象
1. 使用Diagram类对象的Save方法将文件保存到光盘

The following code snippet is a Hello World program to exhibit the working of Aspose.Diagram for Java API. 

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```




