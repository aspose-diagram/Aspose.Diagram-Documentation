---
title: Alanları Güncelle, Kaldır
type: docs
weight: 20
url: /tr/java/update-remove-fields/
description: Bu bölümde alanların nasıl güncelleneceği veya kaldırılacağı açıklanmaktadır.
---
## **Alanı Güncelle**
 Aspose.Diagram for .NET güncellemenizi ve kaldırmanızı sağlar[alan](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio şemaları.

 bu[Alan](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) nesne bir metin alanını temsil eder[Metin](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) koşmak. tarafından gösterilen alan özelliği[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, Aspose.Diagram.Field nesnelerinin bir koleksiyonunu destekler.
### **Programlama Örneği**
Aşağıdaki kod parçası güncelleme alanı şeklindedir.
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

### **Alanı Kaldır**
Aşağıdaki kod parçası, şekildeki alanı kaldırır.
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

