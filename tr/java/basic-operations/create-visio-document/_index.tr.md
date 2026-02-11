---
title: Visio belgesini programlı olarak oluşturun
linktitle: Visio belgesi oluştur
type: docs
weight: 10
url: /tr/java/create-visio-document/
description: Bu sayfada Visio belgesinin Aspose.Diagram kitaplığı ile sıfırdan nasıl oluşturulacağı açıklanmaktadır.
---
## **Yeni Visio Çizimi Oluşturma**
Aspose.Diagram for Java, Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio diyagramlarını okumanızı ve oluşturmanızı sağlar. Yeni belgeler oluştururken ilk adım, bir diagram oluşturmaktır. Ardından, diagram'i oluşturmak için şekiller ve bağlayıcılar ekleyin.
### **Visio Çizim Programlama Örneği Oluşturun**
Aşağıdaki kod, yeni bir Microsoft Visio çizimi oluşturmayı gösterir. Lütfen boş çizimin tek bir boş sayfa içerdiğini unutmayın.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Çizim kağıdı boyutu varsayılan olarak Letter'dır.

{{% /alert %}} 

