---
title: Genel API Aspose.Diagram 6.7.0'daki değişiklikler
type: docs
weight: 20
url: /tr/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

Bu belge, Aspose.Diagram API sürümünde 6.6.0'dan 6.7.0'a modül/uygulama geliştiricilerinin ilgisini çekebilecek değişiklikleri açıklamaktadır. Yalnızca yeni ve güncellenmiş genel yöntemleri değil, aynı zamanda Aspose.Diagram'deki perde arkasındaki davranışlardaki değişikliklerin açıklamasını da içerir.

{{% /alert %}} 
### **FileFormatUtil sınıfında tespitFileFormat yöntemini ekler**
Bir giriş akışında saklanan bir Visio diagram biçimi hakkındaki bilgileri algılar ve döndürür. Lütfen bu kod örneğini kontrol edin:

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
