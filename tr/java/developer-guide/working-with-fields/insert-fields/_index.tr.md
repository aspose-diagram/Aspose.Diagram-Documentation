---
title: Oluştur, Alan ekle
type: docs
weight: 10
url: /tr/java/create-insert-fields/
description: Java Diagram API kullanarak alanlar nasıl oluşturulur, eklenir.
---
## **Alan ekle**
 Aspose.Diagram for Java oluşturmanıza ve eklemenize izin verir[alan](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio şemaları.
### **Programlama Örneği**
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

