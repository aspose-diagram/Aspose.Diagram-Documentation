---
title: 更新、删除字段
type: docs
weight: 20
url: /zh/java/update-remove-fields/
description: 本节说明如何更新或删除字段。
---
## **更新字段**
Aspose.Diagram for .NET 让你更新和删除[场地](https://reference.aspose.com/diagram/java/com.aspose.diagram/field)从您自己的应用程序到 Microsoft Visio 图表，没有 Microsoft Office 自动化。

这[场地](https://reference.aspose.com/diagram/java/com.aspose.diagram/field)object 表示 a 中的文本字段[文本](https://reference.aspose.com/diagram/java/com.aspose.diagram/text)跑。字段属性，由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类支持 Aspose.Diagram.Field 对象的集合。
### **编程范例**
下面这段代码更新字段的形状。
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
```

### **删除字段**
以下代码段删除形状中的字段。
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
```

