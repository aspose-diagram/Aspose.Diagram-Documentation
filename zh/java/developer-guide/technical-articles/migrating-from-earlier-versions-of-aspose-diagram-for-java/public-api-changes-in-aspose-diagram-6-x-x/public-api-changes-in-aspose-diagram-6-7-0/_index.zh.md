---
title: 公共 API Aspose.Diagram 6.7.0 的变化
type: docs
weight: 20
url: /zh/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 6.6.0 到 6.7.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **在 FileFormatUtil 类中添加 detectFileFormat 方法**
它检测并返回有关输入流中存储的 Visio diagram 格式的信息。请检查此代码示例：

**Java**

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Open the stream. Read only access to load a Visio diagram.

InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

// detect file format using an input stream

FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format

System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
