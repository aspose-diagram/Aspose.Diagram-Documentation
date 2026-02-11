---
title: 使用形状段落
type: docs
weight: 40
url: /zh/java/working-with-shapes-paragraph/
---
下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定形状。
1. 设置形状的段落。
#### **设置形状的段落编程示例**
在您的 Java 应用程序中使用以下代码，使用 Aspose.Diagram for Java 设置形状的段落。

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