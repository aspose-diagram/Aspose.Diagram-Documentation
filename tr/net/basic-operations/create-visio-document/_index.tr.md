---
title: Visio belgesini programlı olarak oluşturun
linktitle: Visio belgesi oluştur
type: docs
weight: 10
url: /tr/net/create-visio-document/
description: Bu sayfada Visio belgesinin Aspose.Diagram kitaplığı ile sıfırdan nasıl oluşturulacağı açıklanmaktadır.
---
## **Yeni Visio Çizimi Oluşturma**
Aspose.Diagram for .NET, Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio diyagramlarını okumanızı ve oluşturmanızı sağlar. Yeni belgeler oluştururken ilk adım, bir diagram oluşturmaktır. Ardından, diagram'i oluşturmak için şekiller ve bağlayıcılar ekleyin.
## **Visio Çizim Programlama Örneği Oluşturun**
Aşağıdaki kod, yeni bir Microsoft Visio çizimi oluşturmayı gösterir. Lütfen boş çizimin tek bir boş sayfa içerdiğini unutmayın.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Çizim kağıdı boyutu varsayılan olarak Letter'dır.

{{% /alert %}} 

