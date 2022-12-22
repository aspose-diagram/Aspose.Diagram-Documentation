---
title: Общедоступный API Изменения в Aspose.Diagram 6.7.0
type: docs
weight: 20
url: /ru/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 6.6.0 до 6.7.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Добавляет метод detectFileFormat в класс FileFormatUtil.**
Он обнаруживает и возвращает информацию о формате сохраненного Visio diagram во входном потоке. Пожалуйста, проверьте этот пример кода:

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
