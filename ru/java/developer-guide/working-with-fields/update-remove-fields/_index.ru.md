---
title: Обновить, удалить поля
type: docs
weight: 20
url: /ru/java/update-remove-fields/
description: В этом разделе объясняется, как обновлять или удалять поля.
---
## **Обновить поле**
 Aspose.Diagram for .NET позволяет обновлять и удалять[поле](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) на Microsoft Visio диаграммы из ваших собственных приложений, без автоматизации Microsoft Office.

[Поле](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) объект представляет собой текстовое поле в[текст](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) бегать. Свойство поля, представленное[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class поддерживает набор объектов Aspose.Diagram.Field.
### **Образец программирования**
Следующий фрагмент кода обновляет поле в shape.
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

### **Удалить поле**
Следующий фрагмент кода удаляет поле в форме.
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

