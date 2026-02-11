---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /zh/java/your-first-aspose-diagram-application-hello-world/
description: 本页介绍如何使用 Aspose.Diagram 库创建第一个应用程序。
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. 创建一个实例[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)班级。
1. 如果你有驾照，那么[应用它](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
如果您使用的是评估版，请跳过与许可证相关的代码行。
1. 创建一个新的 Visio 文件，或打开一个现有的 Visio 文件。
1. 创建一个新的文本框。
1. 插入单词**Hello World!**到一个文本框中。
1. 生成修改后的 Microsoft Visio 文件。

下面的示例演示了上述步骤的实现。

### **代码示例：创建一个新的 Diagram**

The following example creates a new diagram from the scratch, writes Hello World! on the first page and saves the Visio file.

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

### **代码示例：打开现有文件**

The following example opens an existing Microsoft Visio template file named "Sample.vsdx", inputs "Hello World!" text in the first page and saves the diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadVisioDiagram.class);   
// Open the stream. Read only access is enough for Aspose.Diagram to load a diagram.
InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

//Call the diagram constructor to load diagram from a VSDX stream
Diagram vsdDiagram = new Diagram(stream);
stream.close();

//Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load diagram from a VSS file
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
